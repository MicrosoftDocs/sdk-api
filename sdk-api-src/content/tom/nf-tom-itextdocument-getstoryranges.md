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

# ITextDocument::GetStoryRanges


## -description


Gets the story collection object used to enumerate the stories in a document. 


## -parameters




### -param ppStories

Type: <b><a href="https://msdn.microsoft.com/eee6c992-1f6a-4e4e-bd8a-34a9aff41859">ITextStoryRanges</a>**</b>

The <a href="https://msdn.microsoft.com/eee6c992-1f6a-4e4e-bd8a-34a9aff41859">ITextStoryRanges</a> pointer.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns the following COM error code. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented; only one story in this document.

</td>
</tr>
</table>
 




## -remarks



Invoke this method only if <a href="https://msdn.microsoft.com/6a9d865c-8710-4e67-bf1a-10d09f81488c">ITextDocument::GetStoryCount</a> returns a value greater than 1.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/6a9d865c-8710-4e67-bf1a-10d09f81488c">GetStoryCount</a>



<a href="https://msdn.microsoft.com/0c3f161f-f6d3-44b9-b041-1b682d1915af">ITextDocument</a>



<a href="https://msdn.microsoft.com/eee6c992-1f6a-4e4e-bd8a-34a9aff41859">ITextStoryRanges</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

