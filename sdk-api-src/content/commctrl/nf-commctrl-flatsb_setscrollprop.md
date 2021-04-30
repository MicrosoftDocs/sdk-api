---
UID: NF:commctrl.FlatSB_SetScrollProp
title: FlatSB_SetScrollProp function (commctrl.h)
description: Sets the properties for a flat scroll bar.
helpviewer_keywords: ["FlatSB_SetScrollProp","FlatSB_SetScrollProp function [Windows Controls]","WSB_PROP_CXHSCROLL","WSB_PROP_CXHTHUMB","WSB_PROP_CXVSCROLL","WSB_PROP_CYHSCROLL","WSB_PROP_CYVSCROLL","WSB_PROP_CYVTHUMB","WSB_PROP_HBKGCOLOR","WSB_PROP_HSTYLE","WSB_PROP_PALETTE","WSB_PROP_VBKGCOLOR","WSB_PROP_VSTYLE","_win32_FlatSB_SetScrollProp","_win32_FlatSB_SetScrollProp_cpp","commctrl/FlatSB_SetScrollProp","controls.FlatSB_SetScrollProp","controls._win32_FlatSB_SetScrollProp"]
old-location: controls\FlatSB_SetScrollProp.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\flatsb\functions\flatsb_setscrollprop.htm
ms.date: 12/05/2018
ms.keywords: FlatSB_SetScrollProp, FlatSB_SetScrollProp function [Windows Controls], WSB_PROP_CXHSCROLL, WSB_PROP_CXHTHUMB, WSB_PROP_CXVSCROLL, WSB_PROP_CYHSCROLL, WSB_PROP_CYVSCROLL, WSB_PROP_CYVTHUMB, WSB_PROP_HBKGCOLOR, WSB_PROP_HSTYLE, WSB_PROP_PALETTE, WSB_PROP_VBKGCOLOR, WSB_PROP_VSTYLE, _win32_FlatSB_SetScrollProp, _win32_FlatSB_SetScrollProp_cpp, commctrl/FlatSB_SetScrollProp, controls.FlatSB_SetScrollProp, controls._win32_FlatSB_SetScrollProp
req.header: commctrl.h
req.include-header: 
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FlatSB_SetScrollProp
 - commctrl/FlatSB_SetScrollProp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - FlatSB_SetScrollProp
---

# FlatSB_SetScrollProp function


## -description

Sets the properties for a flat scroll bar.

## -parameters

### -param unnamedParam1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the window that contains the flat scroll bar. This window handle must have been passed previously in a call to <a href="/windows/desktop/api/commctrl/nf-commctrl-initializeflatsb">InitializeFlatSB</a>.

### -param index

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Determines what 
					<i>newValue</i> represents and which property is being set. This parameter can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WSB_PROP_CXHSCROLL"></a><a id="wsb_prop_cxhscroll"></a><dl>
<dt><b>WSB_PROP_CXHSCROLL</b></dt>
</dl>
</td>
<td width="60%">
<i>newValue</i> is an INT_PTR value that represents the width, in pixels, of the direction buttons in a horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="WSB_PROP_CXHTHUMB"></a><a id="wsb_prop_cxhthumb"></a><dl>
<dt><b>WSB_PROP_CXHTHUMB</b></dt>
</dl>
</td>
<td width="60%">
<i>newValue</i> is an INT_PTR value that represents the width, in pixels, of the thumb in a horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="WSB_PROP_CXVSCROLL"></a><a id="wsb_prop_cxvscroll"></a><dl>
<dt><b>WSB_PROP_CXVSCROLL</b></dt>
</dl>
</td>
<td width="60%">
<i>newValue</i> is an INT_PTR value that represents the width, in pixels, of the vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="WSB_PROP_CYHSCROLL"></a><a id="wsb_prop_cyhscroll"></a><dl>
<dt><b>WSB_PROP_CYHSCROLL</b></dt>
</dl>
</td>
<td width="60%">
<i>newValue</i> is an INT_PTR value that represents the height, in pixels, of the horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="WSB_PROP_CYVSCROLL"></a><a id="wsb_prop_cyvscroll"></a><dl>
<dt><b>WSB_PROP_CYVSCROLL</b></dt>
</dl>
</td>
<td width="60%">
<i>newValue</i> is an INT_PTR value that represents the height, in pixels, of the direction buttons in a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="WSB_PROP_CYVTHUMB"></a><a id="wsb_prop_cyvthumb"></a><dl>
<dt><b>WSB_PROP_CYVTHUMB</b></dt>
</dl>
</td>
<td width="60%">
<i>newValue</i> is an INT_PTR value that represents the height, in pixels, of the thumb in a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="WSB_PROP_HBKGCOLOR"></a><a id="wsb_prop_hbkgcolor"></a><dl>
<dt><b>WSB_PROP_HBKGCOLOR</b></dt>
</dl>
</td>
<td width="60%">
<i>newValue</i> is a 
						<b>COLORREF</b> value that represents the background color in a horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="WSB_PROP_HSTYLE"></a><a id="wsb_prop_hstyle"></a><dl>
<dt><b>WSB_PROP_HSTYLE</b></dt>
</dl>
</td>
<td width="60%">
<i>newValue</i> is one of the following values that changes the visual effects for the horizontal scroll bar. 

<dl>
<dt>FSB_ENCARTA_MODE</dt>
<dd>
A standard flat scroll bar is displayed. When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in 3-D. 

</dd>
<dt>FSB_FLAT_MODE</dt>
<dd>
A standard flat scroll bar is displayed. When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in inverted colors. 

</dd>
<dt>FSB_REGULAR_MODE</dt>
<dd>
A normal, nonflat scroll bar is displayed. No special visual effects will be applied. 

</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="WSB_PROP_PALETTE"></a><a id="wsb_prop_palette"></a><dl>
<dt><b>WSB_PROP_PALETTE</b></dt>
</dl>
</td>
<td width="60%">
<i>newValue</i> is an 
						<b>HPALETTE</b> value that represents the new palette that the scroll bar should use when drawing.

</td>
</tr>
<tr>
<td width="40%"><a id="WSB_PROP_VBKGCOLOR"></a><a id="wsb_prop_vbkgcolor"></a><dl>
<dt><b>WSB_PROP_VBKGCOLOR</b></dt>
</dl>
</td>
<td width="60%">
<i>newValue</i> is a 
						<b>COLORREF</b> value that represents the background color in a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="WSB_PROP_VSTYLE"></a><a id="wsb_prop_vstyle"></a><dl>
<dt><b>WSB_PROP_VSTYLE</b></dt>
</dl>
</td>
<td width="60%">
<i>newValue</i> is one of the following values that changes the visual effects for the vertical scroll bar: 

<dl>
<dt>FSB_ENCARTA_MODE</dt>
<dd>
A standard flat scroll bar is displayed. When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in 3-D. 

</dd>
<dt>FSB_FLAT_MODE</dt>
<dd>
A standard flat scroll bar is displayed. When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in inverted colors. 

</dd>
<dt>FSB_REGULAR_MODE</dt>
<dd>
A normal, nonflat scroll bar is displayed. No special visual effects will be applied. 

</dd>
</dl>
</td>
</tr>
</table>

### -param newValue

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT_PTR</a></b>

A new value to set. This parameter depends on the flag passed in 
					<i>index</i>.

### -param unnamedParam4

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies whether the scroll bar should be redrawn immediately to reflect the change. If this parameter is <b>TRUE</b>, the scroll bar is redrawn; if it is <b>FALSE</b>, the scroll bar is not redrawn.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.

## -remarks

<div class="alert"><b>Note</b>  Flat scroll bar functions are implemented in Comctl32.dll versions 4.71 through 5.82. Comctl32.dll versions 6.00 and higher do not support flat scroll bars.</div>
<div> </div>