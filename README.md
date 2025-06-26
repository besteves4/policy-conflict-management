# Policy conflict management

Description of strategies to be used to solve conflicts that arise from merging multiple policies

## Related work [WIP]

**[ODRL]** Iannella, Renato, and Serena Villata. ‘ODRL Information Model 2.2’. W3C Recommendation 15 February 2018. https://www.w3.org/TR/odrl-model/.

- `odrl:perm`: the Permissions MUST override the Prohibitions
- `odrl:prohibit`: the Prohibitions MUST override the Permissions
- `odrl:invalid`: the entire Policy MUST be void if any conflict is detected

**[Elrakaiby]** Elrakaiby, Yehia, Frédéric Cuppens, and Nora Cuppens-Boulahia. ‘Formal Enforcement and Management of Obligation Policies’. Data & Knowledge Engineering 71, no. 1 (1 January 2012): 127–47. https://doi.org/10.1016/j.datak.2011.09.001.

## Strategies for conflict management

### Rule priority

- **Prioritize Permission**: when there is a Permission rule with the same terms as a Prohibition rule, the *Permission overrides the Prohibition*.
- **Prioritize Prohibition**: when there is a Prohibition rule with the same terms as a Permission rule, the *Prohibition overrides the Permission*.
- **Prioritize Obligation**:
- **Invalid Policies**: when there is a Prohibition rule with the same terms as a Permission rule, the *resulting Policy must be void of any rules*.

- subsumption
- inheritance