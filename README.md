<h1 align="center">Date&&Time</h1>

<p align="center">

<img src="https://img.shields.io/badge/Made%20by-Ogabek-yellow" >

<img src="https://img.shields.io/badge/JavaScript-Lesson%20%236-green">

<img src="https://img.shields.io/badge/Date-&&Time-red">

<img src="https://img.shields.io/badge/Methods-Date-red">

<img src="https://img.shields.io/badge/Learn-Javascript-black">

</p>

---

_In JavaScript, `date and time` are represented by the `Date`object. The Date object provides the date and time information and also provides various methods._

---

>A JavaScript `date` defines the `EcmaScript` epoch that represents milliseconds since `1 January 1970 UTC`. This `date and time` is the same as the `UNIX` epoch (predominant base value for computer-recorded date and time values).

***

<center> <h3>Creating Date Objects</h3></center>

`There are four ways to create a date object.`

* new Date()
* new Date(milliseconds)
* new Date(Date string)
* new Date(year, month, day, hours, minutes, seconds, milliseconds)

---

### new Date()

`You can create a date object using the new Date() constructor.`

```js
const timeNow = new Date();
console.log(timeNow)//Fri Jan 27 2023 14:44:10 GMT+0500 (Узбекистан, стандартное время)
```

>Here, `new Date()` creates a new date object with the current date and local time.

---

### new Date(milliseconds)

`The Date object contains a number that represents milliseconds since 1 January 1970 UTC.`

_`new Date(milliseconds)` creates a new date object by adding the milliseconds to the zero time._

```js
const time = new Date(0);
console.log(time);//Thu Jan 01 1970 06:00:00 GMT+0600 (Узбекистан, стандартное время)

const time2 = new Date(100000000000)
console.log(time2); //Sat Mar 03 1973 15:46:40 GMT+0600 (Узбекистан, стандартное время)
```

>`Note:` 1000 milliseconds is equal to 1 second.

---

### new Date(date string)

`new Date(date string) creates a new date object from a date string.`

__In JavaScript, there are generally three date input formats__

#### ISO Date Formats

`You can create a date object by passing ISO date formats.`

```js
const date = new Date("2023-01-27");
console.log(date); // Fri Jan 27 2023 05:00:00 GMT+0500 (Узбекистан, стандартное время)
```

`You can also pass only the year and month or only the year.`

```js
const date = new Date("2020-07");
console.log(date); // Wed Jul 01 2020 05:00:00 GMT+0500 (Узбекистан, стандартное время)

const date1 = new Date("2020");
console.log(date1);//Wed Jan 01 2020 05:00:00 GMT+0500 (Узбекистан, стандартное время)
```

`You can also pass specific time to ISO dates.`

```js
const date = new Date("2030-01-27T15:18:01Z");
console.log(date);//Fri Jan 27 2023 20:18:00 GMT+0500 (Узбекистан, стандартное время)
```

>__Note:__ Date and time are separated with capital letter `T`. And `UTC` time is defined with capital `Z`.

---

### new Date(year, month, day, hours, minutes, seconds, milliseconds)

`new Date(year, month,...) creates a new date object by passing specific date and time.`

```js
const time1 = new Date(2020, 1, 20, 4, 12, 11, 0);
console.log(time1); // Thu Feb 20 2020 04:12:11
```

>`Note:` If you pass only one argument, it is treated as `milliseconds`. Hence, you have to pass two arguments to use this date format.
`In JavaScript, months are counted from 0 to 11. January is 0 and December is 11.`

---

<center> <h3>Data methods</h3></center>

| _Methods_      | _Description_ |
| ------------   | ----------- |
| __now()__        | Returns the numeric value corresponding to the    current time (the number of milliseconds elapsed since January 1, 1970 00:00:00 UTC)   |
| __getFullYear()__   | Gets the year according to local time        |
| __getMonth()__      | Gets the month, from 0 to 11 according to local time       |
| __getDate()__       | Gets the day of the month (1–31) according to local time        |
| __getDay()__        | Gets the day of the week (0-6) according to local time        |
| __getHours()__      | Gets the hour from 0 to 23 according to local time       |
| __getMinutes()__    | Gets the minute from 0 to 59 according to local time       |
| __getUTCDate()__    | Gets the day of the month (1–31) according to universal time       |
| __setFullYear()__   | Sets the full year according to local time        |
| __setMonth()__      | Sets the month according to local time        |
| __setDate()__       | Sets the day of the month according to local time        |
| __setUTCDate()__    | Sets the day of the month according to universal time       |
