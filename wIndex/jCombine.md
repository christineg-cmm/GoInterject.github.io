---
title: jCombine()
layout: custom
keywords: [jcombine, function]
description: The jCombine() function is helpful for developers who want to concatenate the values of cells while simultaneously skipping any empty cell. 
---
## Function Summary

The jCombine() function is helpful for developers who want to concatenate the values of cells while simultaneously skipping any empty cell. jCombine() can use both a cell range and a list of cell addresses. A list of cell addresses will require a delimiting character between each cell address in the list. The delimiter character can be custom, but it is a comma by default. When using jCombine() in a list of ranges that are not continuous it needs to have a second pair of parentheses around the first set.

### Function Arguments

| Argument Name | Description | Default | Optional |
|----------------|-------------|---------|----------|
|Selected Range |This designates a range of cells from a worksheet that will be concatenated. This can also be used with a delimited list of cells.||NO|
|Delimeter|This defines a character value that will designate a separation between cell values. The default delimiter is a comma.|","|YES|

### Excel Formula Bar Example

```Excel
jCombine((A2,F2:G2,R2:T2))
```
The simplified version of this example is sourced from [Lab Create: Using the Retain Feature](/wGetStarted/L9-Using-The-Retain-Feature.html). In that example jCombine is used as an embedded function but does not have to be. It is often used as a standard Excel function.

### Example Function Composition

| Argument Name | Example Mapping | Explanation |
|---------------|-----------------|-------------|
|Function Name  |=jCombine()    |This is the excel function name used to call the function. It can be used standalone in a report and can be embedded inside of [Data](Data-Functions-Landing.html) or [Formatting](Formatting-Function-Landing.html) functions  |
|Selected Range |(A2,F2:G2,R2:T2)    |In this example, jCombine is concatenating the values of the ranges to look like this: "ValueOfA2,ValueOfF2,ValueOfG2,ValueOfR2,ValueOfS2,ValueOfT2"|
|Delimeter      |" "              |The reason for leaving the delimiting value as blank means that jCombine will use its default comma delimiter. To change the delimiter all you need to do is set a delimiting character value. For example ";".|

### Usable In These Functions

* [Param](Param.html)
* [ReportRange](ReportRange.html) 
* [ReportVariable](ReportVariable.html)
* [ReportFixed](ReportFixed.html)
* [ReportSave](ReportSave.html)
