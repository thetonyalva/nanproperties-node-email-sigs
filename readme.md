## To convert CVS to JSON data
Go here: https://www.convertcsv.com/csv-to-json.htm

Then import the JSON data and choose ``CSV to JSON``.

UPDATE:
I realized that the JSON file was actually an OBJECT, not an ARRAY.

So I had to convert to array using this:

```
  const numbers = {
    one: 1,
  };

  const objectArray = Object.entries(numbers);

  objectArray.forEach(([key, value]) => {
    console.log(key); // 'one'
    console.log(value); // 1
  });
```

But this didn't exactly work to call the end variables outside of the loop.

So I found this:
https://stackoverflow.com/questions/55353908/how-to-call-some-global-variable-from-foreach

and rewrote the script to this:

```
  var agentnamelist = [];

  const objectArray2 = (outerList);
  objectArray2.forEach(values => {

    agentnamelist.push(values["Please enter your Name"])
    
    
  })

console.log(agentnamelist)
```

This will let me call on these arrays in loops to use to populate pages.

Ref:
https://www.samanthaming.com/tidbits/76-converting-object-to-array/

Then I created a new variable referencing the new array, and now I have an array that I can use to manipulate data!

