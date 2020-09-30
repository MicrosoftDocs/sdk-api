---
UID: NS:winuser.tagSCROLLINFO
title: SCROLLINFO (winuser.h)
description: The SCROLLINFO structure contains scroll bar parameters to be set by the SetScrollInfo function (or SBM_SETSCROLLINFO message), or retrieved by the GetScrollInfo function (or SBM_GETSCROLLINFO message).
helpviewer_keywords: ["*LPSCROLLINFO","LPCSCROLLINFO","LPCSCROLLINFO structure pointer [Windows Controls]","SCROLLINFO","SCROLLINFO structure [Windows Controls]","SIF_ALL","SIF_DISABLENOSCROLL","SIF_PAGE","SIF_POS","SIF_RANGE","SIF_TRACKPOS","_win32_SCROLLINFO_str","_win32_SCROLLINFO_str_cpp","controls.SCROLLINFO","controls._win32_SCROLLINFO_str","winuser/LPCSCROLLINFO","winuser/SCROLLINFO"]
old-location: controls\SCROLLINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarstructures\scrollinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPSCROLLINFO, LPCSCROLLINFO, LPCSCROLLINFO structure pointer [Windows Controls], SCROLLINFO, SCROLLINFO structure [Windows Controls], SIF_ALL, SIF_DISABLENOSCROLL, SIF_PAGE, SIF_POS, SIF_RANGE, SIF_TRACKPOS, _win32_SCROLLINFO_str, _win32_SCROLLINFO_str_cpp, controls.SCROLLINFO, controls._win32_SCROLLINFO_str, winuser/LPCSCROLLINFO, winuser/SCROLLINFO'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SCROLLINFO, *LPSCROLLINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSCROLLINFO
 - winuser/tagSCROLLINFO
 - LPSCROLLINFO
 - winuser/LPSCROLLINFO
 - SCROLLINFO
 - winuser/SCROLLINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - SCROLLINFO
---

# SCROLLINFO structure


## -description

The <b>SCROLLINFO</b> structure contains scroll bar parameters to be set by the <a href="/windows/desktop/api/winuser/nf-winuser-setscrollinfo">SetScrollInfo</a> function (or <a href="/windows/desktop/Controls/sbm-setscrollinfo">SBM_SETSCROLLINFO</a> message), or retrieved by the <a href="/windows/desktop/api/winuser/nf-winuser-getscrollinfo">GetScrollInfo</a> function (or <a href="/windows/desktop/Controls/sbm-getscrollinfo">SBM_GETSCROLLINFO</a> message).

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the size, in bytes, of this structure. The caller must set this to sizeof(<b>SCROLLINFO</b>).

### -field fMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the scroll bar parameters to set or retrieve. This member can be a combination of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SIF_ALL"></a><a id="sif_all"></a><dl>
<dt><b>SIF_ALL</b></dt>
</dl>
</td>
<td width="60%">
Combination of SIF_PAGE, SIF_POS, SIF_RANGE, and SIF_TRACKPOS.

</td>
</tr>
<tr>
<td width="40%"><a id="SIF_DISABLENOSCROLL"></a><a id="sif_disablenoscroll"></a><dl>
<dt><b>SIF_DISABLENOSCROLL</b></dt>
</dl>
</td>
<td width="60%">
This value is used only when setting a scroll bar's parameters. If the scroll bar's new parameters make the scroll bar unnecessary, disable the scroll bar instead of removing it. 

</td>
</tr>
<tr>
<td width="40%"><a id="SIF_PAGE"></a><a id="sif_page"></a><dl>
<dt><b>SIF_PAGE</b></dt>
</dl>
</td>
<td width="60%">
The <b>nPage</b> member contains the page size for a proportional scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="SIF_POS"></a><a id="sif_pos"></a><dl>
<dt><b>SIF_POS</b></dt>
</dl>
</td>
<td width="60%">
The <b>nPos</b> member contains the scroll box position, which is not updated while the user drags the scroll box.

</td>
</tr>
<tr>
<td width="40%"><a id="SIF_RANGE"></a><a id="sif_range"></a><dl>
<dt><b>SIF_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The <b>nMin</b> and 
						<b>nMax</b> members contain the minimum and maximum values for the scrolling range.

</td>
</tr>
<tr>
<td width="40%"><a id="SIF_TRACKPOS"></a><a id="sif_trackpos"></a><dl>
<dt><b>SIF_TRACKPOS</b></dt>
</dl>
</td>
<td width="60%">
The <b>nTrackPos</b> member contains the current position of the scroll box while the user is dragging it.

</td>
</tr>
</table>

### -field nMin

Type: <b>int</b>

Specifies the minimum scrolling position.

### -field nMax

Type: <b>int</b>

Specifies the maximum scrolling position.

### -field nPage

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the page size, in device units. A scroll bar uses this value to determine the appropriate size of the proportional scroll box.

### -field nPos

Type: <b>int</b>

Specifies the position of the scroll box.

### -field nTrackPos

Type: <b>int</b>

Specifies the immediate position of a scroll box that the user is dragging. An application can retrieve this value while processing the SB_THUMBTRACK request code. An application cannot set the immediate scroll position; the <a href="/windows/desktop/api/winuser/nf-winuser-setscrollinfo">SetScrollInfo</a> function ignores this member.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getscrollinfo">GetScrollInfo</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/sbm-getscrollinfo">SBM_GETSCROLLINFO</a>



<a href="/windows/desktop/Controls/sbm-setscrollinfo">SBM_SETSCROLLINFO</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setscrollinfo">SetScrollInfo</a>