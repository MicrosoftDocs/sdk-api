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

# ITextSelection::TypeText


## -description


Types the string given by <i>bstr</i> at this selection as if someone typed it. This is similar to the underlying <a href="https://msdn.microsoft.com/26dd5c84-953c-4234-a0b4-53711990bce9">SetText</a> method, but is sensitive to the Insert/Overtype key state and UI settings like AutoCorrect and smart quotes.


## -parameters




### -param bstr

Type: <b>BSTR</b>

String to type into this selection.


## -returns



Type: <b>HRESULT</b>

The method returns an 
						<b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Text is write-protected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
bstr is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -remarks



This method types the string given by <i>bstr</i> at this selection as if someone typed it. Using <b>TypeText</b> is faster than sending characters through the <a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a>
 function, but it is slower than using <a href="https://msdn.microsoft.com/26dd5c84-953c-4234-a0b4-53711990bce9">SetText</a>. 

<b>TypeText</b> is similar to the underlying <a href="https://msdn.microsoft.com/26dd5c84-953c-4234-a0b4-53711990bce9">SetText</a> method, however, it is sensitive to the Insert/Overtype key state and UI settings like AutoCorrect and smart quotes. For example, it deletes any nondegenerate selection and then inserts or overtypes (depending on the Insert/Overtype key state—see the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556703">SetFlags</a> method) the string <i>bstr</i> at the insertion point, leaving this selection as an insertion point following the inserted text. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e6afce18-4f02-4f1c-a2ee-735465d2e168">ITextSelection</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556703">SetFlags</a>



<a href="https://msdn.microsoft.com/26dd5c84-953c-4234-a0b4-53711990bce9">SetText</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

