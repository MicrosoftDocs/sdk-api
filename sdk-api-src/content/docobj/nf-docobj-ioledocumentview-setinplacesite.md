---
UID: NF:docobj.IOleDocumentView.SetInPlaceSite
title: IOleDocumentView::SetInPlaceSite (docobj.h)
description: Associates a container's document view site with a document's view object.
helpviewer_keywords: ["IOleDocumentView interface [COM]","SetInPlaceSite method","IOleDocumentView.SetInPlaceSite","IOleDocumentView::SetInPlaceSite","SetInPlaceSite","SetInPlaceSite method [COM]","SetInPlaceSite method [COM]","IOleDocumentView interface","_ole_ioledocumentview_setinplacesite","com.ioledocumentview_setinplacesite","docobj/IOleDocumentView::SetInPlaceSite"]
old-location: com\ioledocumentview_setinplacesite.htm
tech.root: com
ms.assetid: 88de47c2-979b-4595-8a2f-d4ed1a3a7b6c
ms.date: 12/05/2018
ms.keywords: IOleDocumentView interface [COM],SetInPlaceSite method, IOleDocumentView.SetInPlaceSite, IOleDocumentView::SetInPlaceSite, SetInPlaceSite, SetInPlaceSite method [COM], SetInPlaceSite method [COM],IOleDocumentView interface, _ole_ioledocumentview_setinplacesite, com.ioledocumentview_setinplacesite, docobj/IOleDocumentView::SetInPlaceSite
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
 - IOleDocumentView::SetInPlaceSite
 - docobj/IOleDocumentView::SetInPlaceSite
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
 - IOleDocumentView.SetInPlaceSite
---

# IOleDocumentView::SetInPlaceSite


## -description

Associates a container's document view site with a document's view object.

## -parameters

### -param pIPSite [in]

A pointer to the document view site's <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a> interface. This parameter can be <b>NULL</b>, in which case the document view object loses all asociation with the container.

## -returns

This method returns S_OK if a document view site was successfully associated (or disassociated if <i>pIPSite</i> is <b>NULL</b>) with a document view object. Other possible return values include the following.

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
</table>

## -remarks

As part of activating a document object, a container must pass the object a pointer to the container's implementation of <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>. This pointer designates the document view site that is to be associated with the view on which this method is called.

A container normally passes this pointer in response to a document's request to be activated. A document makes such a request by calling <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentsite-activateme">IOleDocumentSite::ActivateMe</a> and passing the container a pointer to the view to be activated. The container, in turn, uses this pointer to call <b>IOleDocumentView::SetInPlaceSite</b>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
If the container is requesting creation and activation of a new instance of a document object, rather than merely the activation of a loaded instance of a document object, the view site is passed in the <i>pIPSite</i> argument of <a href="/windows/desktop/api/docobj/nf-docobj-ioledocument-createview">IOleDocument::CreateView</a>. Therefore, an explicit call to <b>IOleDocumentView::SetInPlaceSite</b> is unnecessary.


<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If this method is called on a view that is already associated with a view site, the view must do some housekeeping in preparation for activating itself in the new site. First, the view must deactivate itself in the current site and release its pointer to that site. Next, if the new <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a> pointer is not <b>NULL</b>, the view should both save the pointer and call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> on it. The view should then wait for the container to tell it when to activate itself in the new view site.

A document view must implement this method completely; E_NOTIMPL is not an acceptable return value.

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setinplacesite">IOleDocumentView::SetInPlaceSite</a>