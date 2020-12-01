---
UID: NF:docobj.IOleDocumentView.GetRect
title: IOleDocumentView::GetRect (docobj.h)
description: Retrieves the rectangular coordinates of the viewport in which the view is or will be activated.
helpviewer_keywords: ["GetRect","GetRect method [COM]","GetRect method [COM]","IOleDocumentView interface","IOleDocumentView interface [COM]","GetRect method","IOleDocumentView.GetRect","IOleDocumentView::GetRect","_ole_ioledocumentview_getrect","com.ioledocumentview_getrect","docobj/IOleDocumentView::GetRect"]
old-location: com\ioledocumentview_getrect.htm
tech.root: com
ms.assetid: 65d27354-c278-4d9e-b1b7-6fa3651a343d
ms.date: 12/05/2018
ms.keywords: GetRect, GetRect method [COM], GetRect method [COM],IOleDocumentView interface, IOleDocumentView interface [COM],GetRect method, IOleDocumentView.GetRect, IOleDocumentView::GetRect, _ole_ioledocumentview_getrect, com.ioledocumentview_getrect, docobj/IOleDocumentView::GetRect
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
 - IOleDocumentView::GetRect
 - docobj/IOleDocumentView::GetRect
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
 - IOleDocumentView.GetRect
---

# IOleDocumentView::GetRect


## -description

Retrieves the rectangular coordinates of the viewport in which the view is or will be activated.

## -parameters

### -param prcView [out]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure to contain the coordinates of the current viewport set with <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setrect">IOleDocumentView::SetRect</a>.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This view has not yet seen a call to <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setrect">IOleDocumentView::SetRect</a> or <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setrectcomplex">IOleDocumentView::SetRectComplex</a> and therefore has no rectangle to return.

</td>
</tr>
</table>

## -remarks

For a single document interface (SDI) application, the viewport is the client area of the frame window minus the space allocated for toolbars, status bar, and such. For a multiple document interface (MDI) window, the viewport is the client area of the MDI document window minus any other frame-level user-interface elements.

The viewport coordinates obtained by this method are those set in the most recent call to either <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setrect">IOleDocumentView::SetRect</a> or <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setrectcomplex">IOleDocumentView::SetRectComplex</a>.

A document view must implement this method completely; E_NOTIMPL is not an acceptable return value.

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setrect">IOleDocumentView::SetRect</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setrectcomplex">IOleDocumentView::SetRectComplex</a>