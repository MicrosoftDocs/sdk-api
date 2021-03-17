---
UID: NF:docobj.IOleDocumentView.GetInPlaceSite
title: IOleDocumentView::GetInPlaceSite (docobj.h)
description: Retrieves the view site associated with this view object.
helpviewer_keywords: ["GetInPlaceSite","GetInPlaceSite method [COM]","GetInPlaceSite method [COM]","IOleDocumentView interface","IOleDocumentView interface [COM]","GetInPlaceSite method","IOleDocumentView.GetInPlaceSite","IOleDocumentView::GetInPlaceSite","_ole_ioledocumentview_getinplacesite","com.ioledocumentview_getinplacesite","docobj/IOleDocumentView::GetInPlaceSite"]
old-location: com\ioledocumentview_getinplacesite.htm
tech.root: com
ms.assetid: d48cd54c-11b3-4acd-a13a-75a612f1761a
ms.date: 12/05/2018
ms.keywords: GetInPlaceSite, GetInPlaceSite method [COM], GetInPlaceSite method [COM],IOleDocumentView interface, IOleDocumentView interface [COM],GetInPlaceSite method, IOleDocumentView.GetInPlaceSite, IOleDocumentView::GetInPlaceSite, _ole_ioledocumentview_getinplacesite, com.ioledocumentview_getinplacesite, docobj/IOleDocumentView::GetInPlaceSite
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
 - IOleDocumentView::GetInPlaceSite
 - docobj/IOleDocumentView::GetInPlaceSite
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
 - IOleDocumentView.GetInPlaceSite
---

# IOleDocumentView::GetInPlaceSite


## -description

Retrieves the view site associated with this view object.

## -parameters

### -param ppIPSite [out]

A pointer to an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a> pointer variable that receives the interface pointer to the document's view site.

## -returns

This method returns S_OK on success. Other possible values include:

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

<b>IOleDocumentView::GetInPlaceSite</b> obtains the most recent <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a> pointer passed by <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setinplacesite">IOleDocumentView::SetInPlaceSite</a>, or <b>NULL</b> if <b>IOleDocumentView::SetInPlaceSite</b> has not yet been called. If this pointer is not <b>NULL</b>, this method will call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> on the pointer. The caller is responsible for releasing it. A document view must implement this method completely; E_NOTIMPL is not an acceptable return value.

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setinplacesite">IOleDocumentView::SetInPlaceSite</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>