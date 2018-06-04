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

# ITextSelection::SetFlags


## -description


Sets the text selection flags.


## -parameters




### -param Flags

Type: <b>long</b>

New flag values. It can be any combination of the following. 
					

<table class="clsStd">
<tr>
<th>Selection flag</th>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomSelStartActive</b></td>
<td>1</td>
<td>Start end is active.</td>
</tr>
<tr>
<td><b>tomSelAtEOL</b></td>
<td>2</td>
<td>For degenerate selections, the ambiguous 
								character position corresponding to both the beginning of a line and the end of the preceding line should have the caret displayed at the end of the preceding line.</td>
</tr>
<tr>
<td><b>tomSelOvertype</b></td>
<td>4</td>
<td>Insert/Overtype mode is set to overtype. </td>
</tr>
<tr>
<td><b>tomSelActive</b></td>
<td>8</td>
<td>Selection is active.</td>
</tr>
<tr>
<td><b>tomSelReplace</b></td>
<td>16</td>
<td>Typing and pasting replaces selection.</td>
</tr>
</table>
 


Each of the table values is binary. Thus, if any value is not set, the text selection has the opposite property. 


## -returns



Type: <b>HRESULT</b>

The method returns <b>S_OK</b>.




## -remarks



To make sure that the start end is active and that the ambiguous 
				character position is displayed at the end of the line, execute the following code: 

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>selection.Flags = tomSelStartActive + tomSelAtEOL</pre>
</td>
</tr>
</table></span></div>
The 
				Flags property is useful because an <a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a> object can select itself. With <b>SetFlags</b>, you can change the active end from the default value of End, select the caret position for an ambiguous 
				character position, or change the Insert/Overtype mode.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546791">GetFlags</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<a href="https://msdn.microsoft.com/e6afce18-4f02-4f1c-a2ee-735465d2e168">ITextSelection</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

