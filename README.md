### To set up the project:
- Clone the repository
- run npm install
- run npm start


### Note:
#### Instead of the provided Data Model:

export interface Rule {
  field?: 'Theme' | 'Sub-theme' | 'Reason' | 'Language' | 'Source' | 'Rating' | 'Time Period' | 'Customer ID' 
  condition?: 'Equals' | 'Does not equal' | 'Like' | 'Not like' | 'Is Empty' | 'Is' | 'Is not'
  value?: string[]
  type: 'rule'
}
export interface RuleGroup {
  children: (RuleGroup | Rule)[]
  conjunction: 'AND' | 'OR'
  not: boolean
  type: 'rule_group'
}

#### I have used this Data Model: To give the user the ability to delete any filter he wants to.

export interface Rule {
  id: number
  field?: 'Theme' | 'Sub-theme' | 'Reason' | 'Language' | 'Source' | 'Rating' | 'Time Period' | 'Customer ID' 
  condition?: 'Equals' | 'Does not equal' | 'Like' | 'Not like' | 'Is Empty' | 'Is' | 'Is not'
  value?: string[]
  type: 'rule'
}
export interface RuleGroup {
  id: number
  children: (RuleGroup | Rule)[]
  conjunction: 'AND' | 'OR'
  not: boolean
  type: 'rule_group'
}

##### We can check the API output on the console.
