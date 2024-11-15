---
UID: NF:oleidl.IOleInPlaceUIWindow.RequestBorderSpace
title: IOleInPlaceUIWindow::RequestBorderSpace (oleidl.h)
description: Determines whether there is space available for tools to be installed around the object's window frame while the object is active in place.
helpviewer_keywords: ["IOleInPlaceUIWindow interface [COM]","RequestBorderSpace method","IOleInPlaceUIWindow.RequestBorderSpace","IOleInPlaceUIWindow::RequestBorderSpace","RequestBorderSpace","RequestBorderSpace method [COM]","RequestBorderSpace method [COM]","IOleInPlaceUIWindow interface","_ole_ioleinplaceuiwindow_requestborderspace","com.ioleinplaceuiwindow_requestborderspace","oleidl/IOleInPlaceUIWindow::RequestBorderSpace"]
old-location: com\ioleinplaceuiwindow_requestborderspace.htm
tech.root: com
ms.assetid: fd477b1d-e9a5-4b99-adf1-8e62de975730
ms.date: 12/05/2018
ms.keywords: IOleInPlaceUIWindow interface [COM],RequestBorderSpace method, IOleInPlaceUIWindow.RequestBorderSpace, IOleInPlaceUIWindow::RequestBorderSpace, RequestBorderSpace, RequestBorderSpace method [COM], RequestBorderSpace method [COM],IOleInPlaceUIWindow interface, _ole_ioleinplaceuiwindow_requestborderspace, com.ioleinplaceuiwindow_requestborderspace, oleidl/IOleInPlaceUIWindow::RequestBorderSpace
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
 - IOleInPlaceUIWindow::RequestBorderSpace
 - oleidl/IOleInPlaceUIWindow::RequestBorderSpace
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
 - IOleInPlaceUIWindow.RequestBorderSpace
---

# IOleInPlaceUIWindow::RequestBorderSpace


## -description

Determines whether there is space available for tools to be installed around the object's window frame while the object is active in place.

## -parameters

### -param pborderwidths [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)">BORDERWIDTHS</a> structure containing the requested widths (in pixels) needed on each side of the window for the tools.

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
The object cannot install toolbars in this window object because the implementation does not support toolbars, or there is insufficient space to install the toolbars.

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
The active in-place object calls <b>IOleInPlaceUIWindow::RequestBorderSpace</b> to ask if tools can be installed inside the window frame. These tools would be allocated between the rectangle returned by <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-getborder">IOleInPlaceUIWindow::GetBorder</a> and the <a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)">BORDERWIDTHS</a> structure specified in the argument to this call.

The space for the tools is not actually allocated to the object until it calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-setborderspace">IOleInPlaceUIWindow::SetBorderSpace</a>, allowing the object to negotiate for space (such as while dragging toolbars around), but deferring the moving of tools until the action is completed.

The object can install these tools by passing the width in pixels that is to be used on each side. For example, if the object required 10 pixels on the top, 0 pixels on the bottom, and 5 pixels on the left and right sides, it would pass the following <a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)">BORDERWIDTHS</a> structure to <b>IOleInPlaceUIWindow::RequestBorderSpace</b>:


``` syntax
lpbw->top    = 10
lpbw->bottom =  0
lpbw->lLeft  =  5
lpbw->right  =  5
```

<div class="alert"><b>Note</b>  While executing <b>IOleInPlaceUIWindow::RequestBorderSpace</b>, do not make calls to the <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> or <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a> functions, or a dialog box. Doing so may cause the system to deadlock. There are further restrictions on which OLE interface methods and functions can be called from within <b>IOleInPlaceUIWindow::RequestBorderSpace</b>.</div>
<div> </div>
<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the amount of space an active object uses for its toolbars is irrelevant to the container, it can simply return NOERROR as shown in the following <b>IOleInPlaceUIWindow::RequestBorderSpace</b> example. Containers should not unduly restrict the display of tools by an active in-place object.


``` syntax
HRESULT InPlaceUIWindow_RequestBorderSpace( 
    IOleInPlaceFrame *  lpThis, 
    LPCBORDERWIDTHS     pborderwidths) 
{ 
    // Container allows the object to have as much border space as it 
    // wants.  
    return NOERROR; 
} 
```


## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow">IOleInPlaceUIWindow</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-getborder">IOleInPlaceUIWindow::GetBorder</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-setborderspace">IOleInPlaceUIWindow::SetBorderSpace</a>
