---
UID: NF:docobj.IOleDocument.EnumViews
title: IOleDocument::EnumViews
author: windows-sdk-content
description: Creates an object that enumerates the views supported by a document object, or if only one view is supported, returns a pointer to that view.
old-location: com\ioledocument_enumviews.htm
tech.root: com
ms.assetid: ca186853-0792-4a34-b718-46927a73e670
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: EnumViews, EnumViews method [COM], EnumViews method [COM],IOleDocument interface, IOleDocument interface [COM],EnumViews method, IOleDocument.EnumViews, IOleDocument::EnumViews, _ole_ioledocument_enumviews, com.ioledocument_enumviews, docobj/IOleDocument::EnumViews
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IOleDocument.EnumViews
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

