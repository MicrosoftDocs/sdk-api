---
UID: NF:docobj.IOleDocumentView.CloseView
title: IOleDocumentView::CloseView (docobj.h)
description: Instructs a document view to close itself and release its IOleInPlaceSite pointer.
helpviewer_keywords: ["CloseView","CloseView method [COM]","CloseView method [COM]","IOleDocumentView interface","IOleDocumentView interface [COM]","CloseView method","IOleDocumentView.CloseView","IOleDocumentView::CloseView","_ole_ioledocumentview_closeview","com.ioledocumentview_closeview","docobj/IOleDocumentView::CloseView"]
old-location: com\ioledocumentview_closeview.htm
tech.root: com
ms.assetid: d2f443de-929e-4bd4-bfb3-2a28c119c176
ms.date: 12/05/2018
ms.keywords: CloseView, CloseView method [COM], CloseView method [COM],IOleDocumentView interface, IOleDocumentView interface [COM],CloseView method, IOleDocumentView.CloseView, IOleDocumentView::CloseView, _ole_ioledocumentview_closeview, com.ioledocumentview_closeview, docobj/IOleDocumentView::CloseView
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
 - IOleDocumentView::CloseView
 - docobj/IOleDocumentView::CloseView
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
 - IOleDocumentView.CloseView
---

# IOleDocumentView::CloseView


## -description

Instructs a document view to close itself and release its <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a> pointer.

## -parameters

### -param dwReserved [in]

This parameter is reserved and cannot be <b>NULL</b>.

## -returns

This method returns S_OK on success.

## -remarks

When a separate window is no longer needed, the container calls <b>IOleDocumentView::CloseView</b>, whereupon the view releases its site pointer to the separate window and destroys the window. Unlike the normal in-place deactivation sequence for active documents, a document view continues to hold the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a> pointer. This pointer is released only when the view's container calls <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setinplacesite">SetInPlaceSite</a>, with <i>pIPSite</i> set to <b>NULL</b>, or calls <b>IOleDocumentView::CloseView</b>.

When a user closes a view's separate window, the view should not shut itself down. Instead, it should call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-oninplaceactivate">IOleInPlaceSite::OnInPlaceActivate</a>. The view site then decides whether to call <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-uiactivate">IOleDocumentView::UIActivate</a> with <b>FALSE</b> immediately or later. In this way, a document view displayed in a separate window remains available for activation in the container's own window.

The container must call this method before it deletes the view, that is, releases its last reference to the view. In general, implementation of this method will call <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-show">IOleDocumentView::Show</a> with <b>FALSE</b> to hide the view if it is not already hidden, then call <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setinplacesite">SetInPlaceSite</a> with <b>NULL</b> to deactivate itself and release the view site pointer.

Because <b>IOleDocumentView::CloseView</b> is called when a container is going to completely shut down a view, this method must be implemented and has no reason to fail.

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setinplacesite">IOleDocumentView::SetInPlaceSite</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-show">IOleDocumentView::Show</a>