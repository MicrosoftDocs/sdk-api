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

# IOleDocument::EnumViews


## -description


Creates an object that enumerates the views supported by a document object, or if only one view is supported, returns a pointer to that view.


## -parameters




### -param ppEnum [out]

A pointer to an <a href="https://msdn.microsoft.com/cd8fa8b8-17b1-4d77-9611-473725899351">IEnumOleDocumentViews</a> pointer variable that receives the interface pointer to the enumerator object.


### -param ppView [out]

A pointer to an <a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a> pointer variable that receives the interface pointer to a single view object.


## -returns



This method returns S_OK if the object supports multiple views, then <i>ppEnum</i> contains a pointer to the enumerator object, and <i>ppView</i> is <b>NULL</b>. Otherwise, <i>ppEnum</i> is <b>NULL</b>, and <i>ppView</i> contains an interface pointer on the single view.

Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>ppEnum</i> or <i>ppView</i> is invalid. The caller must pass valid pointers for both arguments.

</td>
</tr>
</table>
 




## -remarks



If a document object supports multiple views of its data, it must also implement <a href="https://msdn.microsoft.com/cd8fa8b8-17b1-4d77-9611-473725899351">IEnumOleDocumentViews</a> and pass that interface's pointer in the out parameter <i>ppEnum</i>. Using this pointer, the container can enumerate the views supported by the document object.

If the document object supports only a single view, <b>IOleDocument::EnumViews</b> passes that view's <a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a> pointer in the out parameter <i>ppView</i>.




## -see-also




<a href="https://msdn.microsoft.com/cd8fa8b8-17b1-4d77-9611-473725899351">IEnumOleDocumentViews</a>



<a href="https://msdn.microsoft.com/7a15d6ef-900c-4a0b-8b85-60dc66ca03a3">IOleDocument</a>



<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>
 

 

