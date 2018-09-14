---
UID: NF:docobj.IOleDocument.CreateView
title: IOleDocument::CreateView
author: windows-sdk-content
description: Creates a document view object in the caller's process and obtains a pointer to that object's IOleDocumentView interface.
old-location: com\ioledocument_createview.htm
tech.root: com
ms.assetid: 709d7ff4-d32d-405f-8839-b05df49ef751
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: CreateView, CreateView method [COM], CreateView method [COM],IOleDocument interface, IOleDocument interface [COM],CreateView method, IOleDocument.CreateView, IOleDocument::CreateView, _ole_ioledocument_createview, com.ioledocument_createview, docobj/IOleDocument::CreateView
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
 - IOleDocument.CreateView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleDocument::CreateView


## -description


Creates a document view object in the caller's process and obtains a pointer to that object's <a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a> interface.


## -parameters




### -param pIPSite [in]

A pointer to the <a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a> interface that represents the view site object to be associated with the new document view object. This parameter can be <b>NULL</b>, for example, when the view is contained in a new, uninitialized document object, in which case the caller must initialize the view with a subsequent call to <a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">IOleDocumentView::SetInPlaceSite</a>.


### -param pstm [in]

A pointer to a stream containing data from which the new document view object should initialize itself. If <b>NULL</b>, the document object initializes the new document view object with a default state.


### -param dwReserved [in]

This parameter is reserved and must be zero.


### -param ppView [out]

 A pointer to an <a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a> pointer variable that receives the interface pointer to the new document view object. When successful, the caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> on the <i>ppview</i> pointer when the view object is no longer needed.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>ppView</i> is <b>NULL</b>.


</td>
</tr>
</table>
 




## -remarks



A document object container's document site calls <b>CreateView</b> to instruct a document object to create a new view of itself in the container's process, either from default data or using the contents of an existing stream.

Calling <b>CreateView</b> does not cause the new view to display itself. To do so requires a call to either <a href="https://msdn.microsoft.com/eecc0230-0713-40e9-913c-c51b8a905575">IOleDocumentView::Show</a> or <a href="https://msdn.microsoft.com/df92366c-89b3-44b3-bea0-1b6deb321fe4">IOleDocumentView::UIActivate</a>.





## -see-also




<a href="https://msdn.microsoft.com/7a15d6ef-900c-4a0b-8b85-60dc66ca03a3">IOleDocument</a>



<a href="https://msdn.microsoft.com/4e4a746d-460a-478e-9ca5-be5f63b03d17">IOleDocumentSite::ActivateMe</a>



<a href="https://msdn.microsoft.com/f78526b4-977a-4dde-8a2f-7ae0a1c5c7f9">IOleDocumentView::ApplyViewState</a>



<a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">IOleDocumentView::SetInPlaceSite</a>



<a href="https://msdn.microsoft.com/eecc0230-0713-40e9-913c-c51b8a905575">IOleDocumentView::Show</a>



<a href="https://msdn.microsoft.com/df92366c-89b3-44b3-bea0-1b6deb321fe4">IOleDocumentView::UIActivate</a>
 

 

