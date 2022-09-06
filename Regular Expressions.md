    let date = /\d\d-\d\d-\d\d\d\d/

    console.log(date.test("09-050-2006"))
    // → false
    console.log(/[0-9]/.test("in 1992"))
    // → true
    console.log(/[0-9]/.test("in ma balls"))
    // → false


    // \d	Any digit character
    // \w	An alphanumeric character (“word character”)
    // \s	Any whitespace character (space, tab, newline, and similar)
    // \D	A character that is not a digit
    // \W	A nonalphanumeric character
    // \S	A nonwhitespace character
    // .	Any character except for newline
    // /i 	Makes it case sensitive

    console.log(/'\d+'/.test(" '123' "))
    // → true
    console.log(/'\d*'/.test(" '123' "))
    // → true

    let dateTime = /\d{1,2}-\d{1,2}-\d{4}/;	//limited range
    console.log(dateTime.test("1-30-2003"));
    // → true

    let cartoonCrying = /boo+(hoo+)+/i;		//use ( to add stuff   //the first + applies to the second o in boo and the second o in hoo but the thrid one applies to the whole group 
    console.log(cartoonCrying.test("Boohoooohoohooo"));
    // → true

    let match = /\d+/.exec("one two 100");
    console.log(match);
    console.log(match.index);
    // → 8

    let quotedText = /'([^']*)'/;
    console.log(quotedText.exec("she said 'hello'"))
    console.log(/bad(ly)/.exec("badly"))
    // [ 'badly', 'ly', index: 0, input: 'badly', groups: undefined ]
    console.log(/bad(ly)/.exec("bad"))
    //null

    console.log(new Date())
    console.log(new Date(new Date(2001, 08, 11).getTime()))	//its 9/11!!!!

    console.log(/cat/.test("concatenate"))
    console.log(/\bcat\b/.test("concatenate")) //boundries

    let animalCount = /\b\d+ (pig|cow|chicken)s?\b/;
    console.log(animalCount.test("15 pigs"));		// boundry → digit → "" ("pig"|"cow"|"chicken") → "s" → boundry
    // → true
    console.log(animalCount.test("the 3 pigs"));	// end of a string counts as a boundry
    // → true

    let backtrack = /([01]+)+b/

    console.log(backtrack.test("1100101")) // backtracks through every possible commbination
    console.log(backtrack.test("010010100100101b")) // we good








