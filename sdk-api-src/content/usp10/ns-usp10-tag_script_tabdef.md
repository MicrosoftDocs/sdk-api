---
UID: NS:usp10.tag_SCRIPT_TABDEF
title: tag_SCRIPT_TABDEF
author: windows-driver-content
description: Contains definitions of the tab positions for ScriptStringAnalyse.
old-location: intl\script_tabdef.htm
old-project: Intl
ms.assetid: 023ec258-b3f9-4ea2-8c9d-838df1442068
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: SCRIPT_TABDEF, SCRIPT_TABDEF structure [Internationalization for Windows Applications], _win32_SCRIPT_TABDEF_str, intl.script_tabdef, tag_SCRIPT_TABDEF, usp10/SCRIPT_TABDEF
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: usp10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SCRIPT_TABDEF
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Usp10.h
api_name:
-	SCRIPT_TABDEF
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
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
 

 

