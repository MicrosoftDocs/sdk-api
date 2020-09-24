---
UID: NF:docobj.IOleDocumentView.SetRectComplex
title: IOleDocumentView::SetRectComplex (docobj.h)
description: Sets the rectangular coordinates of the viewport, scroll bars, and size box.
helpviewer_keywords: ["IOleDocumentView interface [COM]","SetRectComplex method","IOleDocumentView.SetRectComplex","IOleDocumentView::SetRectComplex","SetRectComplex","SetRectComplex method [COM]","SetRectComplex method [COM]","IOleDocumentView interface","_ole_ioledocumentview_setrectcomplex","com.ioledocumentview_setrectcomplex","docobj/IOleDocumentView::SetRectComplex"]
old-location: com\ioledocumentview_setrectcomplex.htm
tech.root: com
ms.assetid: d220b200-85cb-43ff-a59d-147c14eef544
ms.date: 12/05/2018
ms.keywords: IOleDocumentView interface [COM],SetRectComplex method, IOleDocumentView.SetRectComplex, IOleDocumentView::SetRectComplex, SetRectComplex, SetRectComplex method [COM], SetRectComplex method [COM],IOleDocumentView interface, _ole_ioledocumentview_setrectcomplex, com.ioledocumentview_setrectcomplex, docobj/IOleDocumentView::SetRectComplex
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
 - IOleDocumentView::SetRectComplex
 - docobj/IOleDocumentView::SetRectComplex
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
 - IOleDocumentView.SetRectComplex
---

# IOleDocumentView::SetRectComplex


## -description

Sets the rectangular coordinates of the viewport, scroll bars, and size box.

## -parameters

### -param prcView [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the coordinates of the viewport.

### -param prcHScroll [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the coordinates of the horizontal scroll bar.

### -param prcVScroll [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the coordinates of the vertical scroll bar.

### -param prcSizeBox [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the coordinates of the size box.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The document object that owns this view does not support complex rectangles.

</td>
</tr>
</table>

## -remarks

View frames that support a workbook metaphor, in which a single document comprises multiple sheets or pages, typically call this method to set the coordinates to be used in common by all the sheets or pages.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Calling <b>IOleDocumentView::SetRectComplex</b> is part of the normal activation sequence for document objects that support complex rectangles, usually following a call to <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-uiactivate">IOleDocumentView::UIActivate</a> and preceding a call to <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-show">IOleDocumentView::Show</a>.

Whenever the window used to display a document object is resized, the container should call <b>IOleDocumentView::SetRectComplex</b> or <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setrect">IOleDocumentView::SetRect</a> to tell the view object to resize itself to the new window dimensions.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Document objects that support complex rectangles mark themselves with <a href="/windows/win32/api/docobj/ne-docobj-docmisc">DOCMISC</a>_SUPPORTCOMPLEXRECTANGLES, as described in <b>DOCMISC</b> and <a href="/windows/desktop/api/docobj/nf-docobj-ioledocument-getdocmiscstatus">IOleDocument::GetDocMiscStatus</a>. Document objects that do not support this method can return E_NOTIMPL.

Upon receiving a call to this method, a view should resize itself to fit the coordinates specified in prcView and fit its scrollbars and size box to the areas described in <i>prcHScroll</i>, <i>prcVScroll</i>, and <i>prcSizeBox</i>.

This method is defined with the [input_sync] attribute, which means that the implementing object cannot yield or make another, non input_sync RPC call while executing this method.

## -see-also

<a href="/windows/desktop/api/docobj/nf-docobj-ioledocument-getdocmiscstatus">IOleDocument::GetDocMiscStatus</a>



<a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a>