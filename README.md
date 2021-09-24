# pacman_lite
MIT PacMan Assignment
v1 something is not right with the code

<p3>Next Tech Comments:</p3>

<p3>Custom TestIncomplete
Pac-man direction reversed </p3>

Test Output

FAIL ./nt-test.js
  checkPageBounds()
    ✓ should reverse direction (2 ms)
    ✕ should reverse direction (3 ms)
    ✕ should not reverse direction (1 ms)

  ● checkPageBounds() › should reverse direction

    expect(received).toBe(expected) // Object.is equality

    Expected: 0
    Received: 1

      11 |   });
      12 |   it ('should reverse direction', function () {  
    > 13 |     expect(checkPageBounds(1, 10,-20,100)).toBe(0);
         |                                            ^
      14 |   });
      15 |   it ('should not reverse direction', function () {  
      16 |     expect(checkPageBounds(1, 10,0,100)).toBe(1);

      at Object.<anonymous> (nt-test.js:13:44)

  ● checkPageBounds() › should not reverse direction

    expect(received).toBe(expected) // Object.is equality

    Expected: 1
    Received: 0

      14 |   });
      15 |   it ('should not reverse direction', function () {  
    > 16 |     expect(checkPageBounds(1, 10,0,100)).toBe(1);
         |                                          ^
      17 |   });
      18 | });

      at Object.<anonymous> (nt-test.js:16:42)

Test Suites: 1 failed, 1 total
Tests:       2 failed, 1 passed, 3 total
Snapshots:   0 total
Time:        4.81 s
Ran all test suites matching /nt-test.js/i.
Test Contents
/**
 * @jest-environment jsdom
 */


var checkPageBounds = require('./pacman.js');

describe ('checkPageBounds()', function () {
  it ('should reverse direction', function () {
    expect(checkPageBounds(0, 10,100,100)).toBe(1);
  });
  it ('should reverse direction', function () {  
    expect(checkPageBounds(1, 10,-20,100)).toBe(0);
  });
  it ('should not reverse direction', function () {  
    expect(checkPageBounds(1, 10,0,100)).toBe(1);
  });
});



<p3>Code PatternIncomplete</p3>
Add a setInterval call to run every 200 millesecs

Description
Searched your code for a specific pattern:

setInterval\([a-zA-Z].*,\s*200\)
