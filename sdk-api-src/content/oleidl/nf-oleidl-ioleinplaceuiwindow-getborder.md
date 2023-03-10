---
UID: NF:oleidl.IOleInPlaceUIWindow.GetBorder
title: IOleInPlaceUIWindow::GetBorder (oleidl.h)
description: Retrieves the outer rectangle for toolbars and controls while the object is active in place.
helpviewer_keywords: ["GetBorder","GetBorder method [COM]","GetBorder method [COM]","IOleInPlaceUIWindow interface","IOleInPlaceUIWindow interface [COM]","GetBorder method","IOleInPlaceUIWindow.GetBorder","IOleInPlaceUIWindow::GetBorder","_ole_ioleinplaceuiwindow_getborder","com.ioleinplaceuiwindow_getborder","oleidl/IOleInPlaceUIWindow::GetBorder"]
old-location: com\ioleinplaceuiwindow_getborder.htm
tech.root: com
ms.assetid: 9ee9970a-b937-4538-b3b8-460647086db1
ms.date: 12/05/2018
ms.keywords: GetBorder, GetBorder method [COM], GetBorder method [COM],IOleInPlaceUIWindow interface, IOleInPlaceUIWindow interface [COM],GetBorder method, IOleInPlaceUIWindow.GetBorder, IOleInPlaceUIWindow::GetBorder, _ole_ioleinplaceuiwindow_getborder, com.ioleinplaceuiwindow_getborder, oleidl/IOleInPlaceUIWindow::GetBorder
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IOleInPlaceUIWindow::GetBorder
 - oleidl/IOleInPlaceUIWindow::GetBorder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleInPlaceUIWindow.GetBorder
---

# IOleInPlaceUIWindow::GetBorder


## -description

Retrieves the outer rectangle for toolbars and controls while the object is active in place.

## -parameters

### -param lprectBorder [out]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure where the outer rectangle is to be returned. The structure's coordinates are relative to the window being represented by the interface.

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
<dt><b>INPLACE_E_NOTOOLSPACE</b></dt>
</dl>
</td>
<td width="60%">
The object cannot install toolbars in this window object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for this operation.

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
</table>

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The <b>IOleInPlaceUIWindow::GetBorder</b> function, when called on a document or frame window object, returns the outer rectangle (relative to the window) where the object can put toolbars or similar controls.

If the object is to install these tools, it should negotiate space for the tools within this rectangle using <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-requestborderspace">IOleInPlaceUIWindow::RequestBorderSpace</a> and then call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-setborderspace">IOleInPlaceUIWindow::SetBorderSpace</a> to get this space allocated.

<div class="alert"><b>Note</b>  While executing <b>IOleInPlaceUIWindow::GetBorder</b>, do not make calls to the <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> or <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a> functions, or a dialog box. Doing so may cause the system to deadlock. There are further restrictions on which OLE interface methods and functions can be called from within <b>GetBorder</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow">IOleInPlaceUIWindow</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-requestborderspace">IOleInPlaceUIWindow::RequestBorderSpace</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-setborderspace">IOleInPlaceUIWindow::SetBorderSpace</a>