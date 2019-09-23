# Tests
This folder includes the tests for all scoring methods.

All tests can be run with: `yarn test`

**Tests for:**
- 0. Error
- 1. Functionality
- 2. Cases

---

## Score
`level, suit, double, declarer, vulnerability, result -> Score`

#### Tests

- [x] 0.1. Error - level invalid
- [x] 0.2. Error - suit invalid
- [x] 0.3. Error - double invalid
- [x] 0.4. Error - declarer invalid
- [x] 0.5. Error - vulnerability invalid
- [x] 0.6. Error - result invalid
- [x] 1.1. Func - Gamebonus
- [x] 1.2. Func - Slambonus
- [x] 1.3. Func - Double / Redouble
- [x] 1.4. Func - Vulnerability
- [x] 1.5. Func - Declarer / Result
- [x] 2.0. Case - Extreme Results
- [x] 2.1. Case - all results: 1 club
- [x] 2.2. Case - all results: 1 diamond"
---

## Matchpoints
Different methods for calculating *matchpoints* are implemented and tested.

### scoresToMatchpoints
`List of Scores -> List of Matchpoints`

#### Tests

- [x] 1.1. Func - Empty list
- [x] 1.2. Func - Single item in list
- [x] 2.1. Case - [-90,170,-90,-100,-90,150]
- [x] 2.2. Case - [150, 120, 120, 430, 400, 400]
- [x] 2.3. Case - [170, 170, 170, 170, 150, 150]
- [x] 2.4. Case - [200, -170, -450, -150, -170, -170, 50, -170, -100]
- [x] 2.5. Case - [-110, -170, -120, -200, 200, 0, 0, -300, 100]

### matchpointsToPercentages
`List of Matchpoints -> List of Percentages`

#### Tests

- [x] 1.1. Func - Empty list
- [x] 1.2. Func - Single item in list
- [x] 2.1. Case - [0,2,4]
- [x] 2.2. Case - [1,1,4,7,7]
- [x] 2.3. Case - [7,7,7,7,1,1]

### matchpointsReverse
`List of Matchpoints -> List of reverse Matchpoints`

#### Tests
- [x] 1.1. Func - Empty list
- [x] 1.2. Func - Single item in list
- [x] 2.1. Case - [-90,170,-90,-100,-90,150]
- [x] 2.2. Case - [150, 120, 120, 430, 400, 400]
- [x] 2.3. Case - [170, 170, 170, 170, 150, 150]
- [x] 2.4. Case - [200, -170, -450, -150, -170, -170, 50, -170, -100]
- [x] 2.5. Case - [-110, -170, -120, -200, 200, 0, 0, -300, 100]
- [x] 2.6. Case - [0,2,4,6,8]
- [x] 2.7. Case - [1,1,4,7,7]

---

## IMPs
`ScoreDifference -> IMPs` has been tested for every value from -10.000 to 10.000.

#### Tests
- [x] 0.1. Error - score difference invalid
- [x] 0.2. Error - score difference invalid range
- [x] 1.1. Func - Positive & negative Scoredifference
- [x] 2.0. Case - Score difference = +/- [0,10]
- [x] 2.1. Case - Score difference = +/- [30,40]
- [x] 2.2. Case - Score difference = +/- [50,80]
- [x] 2.3. Case - Score difference = +/- [90,120]
- [x] 2.4. Case - Score difference = +/- [130,160]
- [x] 2.5. Case - Score difference = +/- [170,210]
- [x] 2.6. Case - Score difference = +/- [220,260]
- [x] 2.7. Case - Score difference = +/- [270,310]
- [x] 2.8. Case - Score difference = +/- [320,360]
- [x] 2.9. Case - Score difference = +/- [370,420]
- [x] 2.10. Case - Score difference = +/- [430,490]
- [x] 2.11. Case - Score difference = +/- [500,590]
- [x] 2.12. Case - Score difference = +/- [600,740]
- [x] 2.13. Case - Score difference = +/- [750,890]
- [x] 2.14. Case - Score difference = +/- [900,1090]
- [x] 2.15. Case - Score difference = +/- [1100,1290]
- [x] 2.16. Case - Score difference = +/- [1300,1490]
- [x] 2.17. Case - Score difference = +/- [1500,1740]
- [x] 2.18. Case - Score difference = +/- [1750,1990]
- [x] 2.19. Case - Score difference = +/- [2000,2240]
- [x] 2.20. Case - Score difference = +/- [2250,2490]
- [x] 2.21. Case - Score difference = +/- [2500,2990]
- [x] 2.22. Case - Score difference = +/- [3000,3490]
- [x] 2.23. Case - Score difference = +/- [3500,3990]
- [x] 2.24. Case - Score difference = +/- [4000,9990]
- [x] 2.25. Case - Score difference wrong

---

## Victory Points
`IMPs -> Victory Points` is calculated but compared to the official formula table from the World Bridge Federation (WBF).
Further validation testing is therefor pointless.

#### Tests
- [x] 0.1. Error - IMPs invalid
- [x] 0.2. Error - boardCnt invalid
- [x] 0.3. Error - boardCnt invalid range
- [x] 2.1. Case - IMPS: 16, Boards: 32
- [x] 2.2. Case - IMPs: 47, Boards: 32