# Evaluation

- **Status:** In Progress
- **Application Document:**  clickme
- **Milestone:** 2
- **Kusama Identity:** [ESxS4A7GHMLzve4Mbc9t27RpXtVTnV3LtcMTtcnD26jcUHA](https://polkascan.io/pre/kusama/account/ESxS4A7GHMLzve4Mbc9t27RpXtVTnV3LtcMTtcnD26jcUHA)
- **Previously successfully merged evaluation:** All by semuelle

| Number | Deliverable | Accepted | Link | Evaluation Notes |
| ------ | ----------- | :------: | ---- |----------------- |
| 0a. | License | <ul><li>[x] </li></ul> | [UniversalDot/universal-dot-front-end](https://github.com/UniversalDot/universal-dot-front-end/blob/b3d4777679c97e27233cb876ff56ee4e0b993a39/LICENSE) | Unlicense
| 0b. | Documentation | <ul><li>[x] </li></ul> | [UniversalDot/pallets](https://github.com/UniversalDot/pallets/tree/f0be4fb09350a8177263702bf8e8ac7cf4afcd92) | Very good inline documentation. |
| 0c. | Testing Guide | <ul><li>[ ] </li></ul> | [UniversalDot/universal-dot-front-end](https://github.com/UniversalDot/universal-dot-front-end/tree/b3d4777679c97e27233cb876ff56ee4e0b993a39#testing) | Guide is easy to follow, but some tests fail. See [General Notes](#general-notes) |
| 0d. | Docker | <ul><li>[x] </li></ul> | [UniversalDot/compose-service](https://github.com/UniversalDot/compose-service/tree/9f6c53ea504345ea974d8650e5005bf82e537340#compose-service) | — |
| 0e. | Article | <ul><li>[x] </li></ul> | [USER-MANUAL.md](https://github.com/UniversalDot/universal-dot-front-end/blob/b3d4777679c97e27233cb876ff56ee4e0b993a39/USER-MANUAL.md) | —
| 1. | React module: Profile | <ul><li>[ ] </li></ul> | [components/profile-configuration](https://github.com/UniversalDot/universal-dot-front-end/blob/b3d4777679c97e27233cb876ff56ee4e0b993a39/src/components/profile-configuration/ProfileConfiguration.jsx) | See [General Notes](#general-notes) |  
| 2. | React module: Task | <ul><li>[ ] </li></ul> | [components/task](https://github.com/UniversalDot/universal-dot-front-end/blob/b3d4777679c97e27233cb876ff56ee4e0b993a39/src/components/task/Task.jsx) | See [General Notes](#general-notes) |  
| 3. | React module: DAO | <ul><li>[ ] </li></ul> | [components/organizations](https://github.com/UniversalDot/universal-dot-front-end/blob/b3d4777679c97e27233cb876ff56ee4e0b993a39/src/components/organizations/Organizations.jsx) | See [General Notes](#general-notes) |
| 4. | App module | <ul><li>[x] </li></ul> | [UniversalDot/universal-dot-front-end](https://github.com/UniversalDot/universal-dot-front-end/tree/b3d4777679c97e27233cb876ff56ee4e0b993a39) | see also https://universaldot.me |
| 5. | Substrate chain (mainnet) | <ul><li>[x] </li></ul> | wss://3lnc.l.time4vps.cloud:443 | — |


## General Notes

- `yarn npm audit` reports some `high` and `critical` issues
- 3/4 `profile` tests fail:
  - 2/4: `Timed out retrying after 4000ms: Expected to find element: div.ui.info.message div.header, but never found it.`
  - 3/4 + 4/4: `cy.type() can only be called on a single element. Your subject contained 2 elements.`
- No input validation on forms. For example, the UI showed an infinite loading animation after creating a task with a budget of `-1`.
