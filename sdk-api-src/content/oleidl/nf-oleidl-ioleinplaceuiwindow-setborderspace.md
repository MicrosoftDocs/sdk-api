---
UID: NF:oleidl.IOleInPlaceUIWindow.SetBorderSpace
title: IOleInPlaceUIWindow::SetBorderSpace (oleidl.h)
description: Allocates space for the border requested in the call to IOleInPlaceUIWindow::RequestBorderSpace.
helpviewer_keywords: ["IOleInPlaceUIWindow interface [COM]","SetBorderSpace method","IOleInPlaceUIWindow.SetBorderSpace","IOleInPlaceUIWindow::SetBorderSpace","SetBorderSpace","SetBorderSpace method [COM]","SetBorderSpace method [COM]","IOleInPlaceUIWindow interface","_ole_ioleinplaceuiwindow_setborderspace","com.ioleinplaceuiwindow_setborderspace","oleidl/IOleInPlaceUIWindow::SetBorderSpace"]
old-location: com\ioleinplaceuiwindow_setborderspace.htm
tech.root: com
ms.assetid: 7c806a02-db6d-444e-a049-22c4ae2b19b0
ms.date: 12/05/2018
ms.keywords: IOleInPlaceUIWindow interface [COM],SetBorderSpace method, IOleInPlaceUIWindow.SetBorderSpace, IOleInPlaceUIWindow::SetBorderSpace, SetBorderSpace, SetBorderSpace method [COM], SetBorderSpace method [COM],IOleInPlaceUIWindow interface, _ole_ioleinplaceuiwindow_setborderspace, com.ioleinplaceuiwindow_setborderspace, oleidl/IOleInPlaceUIWindow::SetBorderSpace
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
 - IOleInPlaceUIWindow::SetBorderSpace
 - oleidl/IOleInPlaceUIWindow::SetBorderSpace
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
 - IOleInPlaceUIWindow.SetBorderSpace
---

# IOleInPlaceUIWindow::SetBorderSpace


## -description

Allocates space for the border requested in the call to <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-requestborderspace">IOleInPlaceUIWindow::RequestBorderSpace</a>.

## -parameters

### -param pborderwidths [in]

Pointer to a <a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)">BORDERWIDTHS</a> structure containing the requested width of the tools, in pixels. It can be <b>NULL</b>, indicating the object does not need any space.

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
<dt><b>OLE_E_INVALIDRECT</b></dt>
</dl>
</td>
<td width="60%">
The rectangle does not lie within the specifications returned by <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-getborder">IOleInPlaceUIWindow::GetBorder</a>.

</td>
</tr>
</table>

## -remarks

The object must call <b>IOleInPlaceUIWindow::SetBorderSpace</b>. It can do any one of the following:

<ul>
<li>Use its own toolbars, requesting border space of a specific size.</li>
<li>Use no toolbars, but force the container to remove its toolbars by passing a valid <a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)">BORDERWIDTHS</a> structure containing nothing but zeros in the <i>pborderwidths</i> parameter.</li>
<li>Use no toolbars but allow the in-place container to leave its toolbars up by passing <b>NULL</b> as the <i>pborderwidths</i> parameter.</li>
</ul>
The <a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)">BORDERWIDTHS</a> structure used in this call would generally have been passed in a previous call to <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-requestborderspace">IOleInPlaceUIWindow::RequestBorderSpace</a>, which must have returned S_OK.

If an object must renegotiate space on the border, it can call <b>IOleInPlaceUIWindow::SetBorderSpace</b> again with the new widths. If the call to <b>IOleInPlaceUIWindow::SetBorderSpace</b> fails, the object can do a full negotiation for border space with calls to <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-getborder">IOleInPlaceUIWindow::GetBorder</a>, <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-requestborderspace">IOleInPlaceUIWindow::RequestBorderSpace</a>, and <b>IOleInPlaceUIWindow::SetBorderSpace</b>.

<div class="alert"><b>Note</b>  While executing <b>IOleInPlaceUIWindow::SetBorderSpace</b>, do not make calls to the <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> or <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a> functions, or a dialog box. Doing so may cause the system to deadlock. There are further restrictions on which OLE interface methods and functions can be called from within <b>IOleInPlaceUIWindow::SetBorderSpace</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow">IOleInPlaceUIWindow</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-getborder">IOleInPlaceUIWindow::GetBorder</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-requestborderspace">IOleInPlaceUIWindow::RequestBorderSpace</a>