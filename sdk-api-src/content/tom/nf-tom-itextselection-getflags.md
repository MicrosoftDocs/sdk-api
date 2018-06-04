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

# ITextSelection::GetFlags


## -description


Gets the text selection flags.


## -parameters




### -param pFlags

Type: <b>long*</b>

Any combination of the following selection flags.
               

<table class="clsStd">
<tr>
<th>Selection Flag</th>
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

The method returns an 
						<b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>pFlags</i> is null, the method fails and it returns E_INVALIDARG.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<a href="https://msdn.microsoft.com/e6afce18-4f02-4f1c-a2ee-735465d2e168">ITextSelection</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556703">SetFlags</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

