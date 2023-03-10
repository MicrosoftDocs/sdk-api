---
UID: NF:docobj.IOleDocument.CreateView
title: IOleDocument::CreateView (docobj.h)
description: Creates a document view object in the caller's process and obtains a pointer to that object's IOleDocumentView interface.
helpviewer_keywords: ["CreateView","CreateView method [COM]","CreateView method [COM]","IOleDocument interface","IOleDocument interface [COM]","CreateView method","IOleDocument.CreateView","IOleDocument::CreateView","_ole_ioledocument_createview","com.ioledocument_createview","docobj/IOleDocument::CreateView"]
old-location: com\ioledocument_createview.htm
tech.root: com
ms.assetid: 709d7ff4-d32d-405f-8839-b05df49ef751
ms.date: 12/05/2018
ms.keywords: CreateView, CreateView method [COM], CreateView method [COM],IOleDocument interface, IOleDocument interface [COM],CreateView method, IOleDocument.CreateView, IOleDocument::CreateView, _ole_ioledocument_createview, com.ioledocument_createview, docobj/IOleDocument::CreateView
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleDocument::CreateView
 - docobj/IOleDocument::CreateView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IOleDocument.CreateView
---

# IOleDocument::CreateView


## -description

Creates a document view object in the caller's process and obtains a pointer to that object's <a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a> interface.

## -parameters

### -param pIPSite [in]

A pointer to the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a> interface that represents the view site object to be associated with the new document view object. This parameter can be <b>NULL</b>, for example, when the view is contained in a new, uninitialized document object, in which case the caller must initialize the view with a subsequent call to <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setinplacesite">IOleDocumentView::SetInPlaceSite</a>.

### -param pstm [in]

A pointer to a stream containing data from which the new document view object should initialize itself. If <b>NULL</b>, the document object initializes the new document view object with a default state.

### -param dwReserved [in]

This parameter is reserved and must be zero.

### -param ppView [out]

 A pointer to an <a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a> pointer variable that receives the interface pointer to the new document view object. When successful, the caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the <i>ppview</i> pointer when the view object is no longer needed.

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

Calling <b>CreateView</b> does not cause the new view to display itself. To do so requires a call to either <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-show">IOleDocumentView::Show</a> or <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-uiactivate">IOleDocumentView::UIActivate</a>.

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-ioledocument">IOleDocument</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentsite-activateme">IOleDocumentSite::ActivateMe</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-applyviewstate">IOleDocumentView::ApplyViewState</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setinplacesite">IOleDocumentView::SetInPlaceSite</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-show">IOleDocumentView::Show</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-uiactivate">IOleDocumentView::UIActivate</a>