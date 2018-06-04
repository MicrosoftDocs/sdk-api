---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tag_SCRIPT_TABDEF structure


## -description



Contains definitions of the tab positions for <a href="https://msdn.microsoft.com/6d0e7070-159e-436b-85b5-cabb3da83f5e">ScriptStringAnalyse</a>.




## -struct-fields




### -field cTabStops

Number of entries in the array indicated by <b>pTabStops</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>Tab stops occur every eight average character widths.</td>
</tr>
<tr>
<td>1</td>
<td>All tab stops are the length of the first entry in the array indicated by <b>pTabStops</b>.</td>
</tr>
<tr>
<td>greater than 1</td>
<td>The first <b>cTabStops</b> tab stops are as specified in the array indicated by <b>pTabStops</b>, and subsequent tab stops are every eight average characters.</td>
</tr>
</table>
 


### -field iScale

Scale factor for <b>iTabOrigin</b> and <b>pTabStops</b> values. Values are converted to device coordinates by multiplying by the value indicated by <b>iScale</b>, then dividing by 4. If values are already in device units, set <b>iScale</b> to 4. If values are in dialog units, set <b>iScale</b> to the average character width of the dialog font. If values are multiples of the average character width for the selected font, set <b>iScale</b> to 0.


### -field pTabStops

Pointer to an array having the number of entries indicated by <b>cTabStops</b>. Each entry specifies a tab stop position. Positive values represent near-edge alignment, while negative values represent far-edge alignment. The units for the array elements are as indicated by the value of <b>iScale</b>.


### -field iTabOrigin

Initial offset, in logical units, for tab stops. Tabs start <b>iTabOrigin</b> logical units before the beginning of the string. This rule helps with situations in which multiple tabbed outputs occur on the same line.


## -remarks



This structure is ignored unless the <i>dwFlags</i> parameter is set to SSA_TAB in the       <a href="https://msdn.microsoft.com/6d0e7070-159e-436b-85b5-cabb3da83f5e">ScriptStringAnalyse</a> function.




## -see-also




<a href="https://msdn.microsoft.com/6d0e7070-159e-436b-85b5-cabb3da83f5e">ScriptStringAnalyse</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/243438fd-5bb2-4b2a-8b33-803029085adb">Uniscribe Structures</a>
 

 

