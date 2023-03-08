---
UID: NF:docobj.IOleDocumentView.Open
title: IOleDocumentView::Open (docobj.h)
description: Displays a document view in a separate pop-up window. The semantics are equivalent to IOleObject::DoVerb with OLEIVERB_OPEN.
helpviewer_keywords: ["IOleDocumentView interface [COM]","Open method","IOleDocumentView.Open","IOleDocumentView::Open","Open","Open method [COM]","Open method [COM]","IOleDocumentView interface","_ole_ioledocumentview_open","com.ioledocumentview_open","docobj/IOleDocumentView::Open"]
old-location: com\ioledocumentview_open.htm
tech.root: com
ms.assetid: 46f801ae-ae03-4567-9442-cf3fbb6d06d7
ms.date: 12/05/2018
ms.keywords: IOleDocumentView interface [COM],Open method, IOleDocumentView.Open, IOleDocumentView::Open, Open, Open method [COM], Open method [COM],IOleDocumentView interface, _ole_ioledocumentview_open, com.ioledocumentview_open, docobj/IOleDocumentView::Open
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
 - IOleDocumentView::Open
 - docobj/IOleDocumentView::Open
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
 - IOleDocumentView.Open
---

# IOleDocumentView::Open


## -description

Displays a document view in a separate pop-up window. The semantics are equivalent to <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-doverb">IOleObject::DoVerb</a> with OLEIVERB_OPEN.



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
Insufficient memory  available for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The document object that owns this view does not support separate window activation.

</td>
</tr>
</table>

## -remarks

A user viewing a document object in a container application such as a browser or "binder" may want to see two or more views or documents at once. Because the browser displays only one view at a time, the container needs a way to ask the other views or documents to display themselves, as required, in separate windows. The <b>IOleDocumentView::Open</b> method provides that way.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A successful call to <b>IOleDocumentView::Open</b> should be followed by a call to <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-show">IOleDocumentView::Show</a> to hide the window or to show the window and bring it to the foreground. While the view is active in its separate window, a container can show or hide the window as many times as it may require.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
A document object indicates that it does not support activation in a separate window by setting the <a href="/windows/win32/api/docobj/ne-docobj-docmisc">DOCMISC</a>_CANTOPENEDIT status flag and returning E_NOTIMPL to containers that call this method.

Implementation consists mainly of the view object calling its own <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-inplacedeactivate">IOleInPlaceObject::InPlaceDeactivate</a> method, which leaves the document object in a running state but without in-place activation. The document object's user interface is not visible until the container calls <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-show">IOleDocumentView::Show</a> (see Notes to Callers above).

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-closeview">IOleDocumentView::CloseView</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-show">IOleDocumentView::Show</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-uiactivate">IOleDocumentView::UIActivate</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-inplacedeactivate">IOleInPlaceObject::InPlaceDeactivate</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-oninplaceactivate">IOleInPlaceSite::OnInPlaceActivate</a>
