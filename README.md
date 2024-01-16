# An Empirical Study on Cross-language Mirror Bugs

---

## Project summary

Many applications have implementations in different languages. Although their languages are different, they can implement similar or even identical functionalities. If an implementation has a bug, the other implementations can have corresponding bugs. In this paper, we call them cross-language clone bugs, or mirror bugs for short. Mirror bugs are important since many applications release implementations in different languages. From mirror bugs, it can be feasible to learn more bug patterns, and thus detect more types of bugs. Although researchers have conducted empirical studies to analyze the bugs in clones, to the best of our knowledge, no study has ever explored mirror bugs. As a result, many research questions are still open. For example, are there any mirror bugs in real projects? Are bug fixes in a language useful to detect and repair bugs in other languages? To answer the above questions, in this paper, we conduct the first empirical study on mirror bugs. In this study, we manually analyze 402 bugs that are collected from four projects, and each project releases a Java implementation and C\# implementation. Our study presents answers to two interesting research questions. According to our results, there is a timely need for a tool that assists in detecting mirror bugs. Indeed, we find that some programmers already manually identify and fix mirror bugs, even without any tool support.

---
## Dataset

We collect 402 bug reports from 4 project pairs. For details, see [all_bugs.txt](https://github.com/chenhh021/cross-language-poster/blob/main/all_bugs.txt) for the whole set; [two_sided_bugs.md](https://github.com/chenhh021/cross-language-poster/blob/main/two_sided_bugs.md) for fixed two-sided bugs.

---

## Categories

We classified sample bugs into different categories listed below.

| Type Id | Type Name | Description |
| ------- | --------- | -----------------------------------|
| T1      | Two-sided Bug|  Bugs appear in both Java and C# implementations |
| T1.1    | Fixed Two-sided Bug| Two-sided bugs fixed on both sides |
| T1.1.1  | Reported Two-sided Bug| Fixed two-sided bugs with reports on both sides |
| T1.1.2  | Identified Two-sided Bug| Fixed two-sided bugs with report on either Java or C\# side|
| T1.2    | Unfixed Two-sided Bug| Two-sided bugs fixed on either Java or C\# side|
| T1.2.1  | Potential Bug| unfixed Bugs with serious symptoms |
| T1.2.2  | Bug with Minor Symptoms| Unfixed bug with minor symptoms |
| T2      | One-sided Bug | Bugs appear in either Java or C# implementation|
