---
UID: NF:winuser.DrawCaption
title: DrawCaption function (winuser.h)
description: The DrawCaption function draws a window caption.
helpviewer_keywords: ["DC_ACTIVE","DC_BUTTONS","DC_GRADIENT","DC_ICON","DC_INBUTTON","DC_SMALLCAP","DC_TEXT","DrawCaption","DrawCaption function [Windows GDI]","_win32_DrawCaption","gdi.drawcaption","winuser/DrawCaption"]
old-location: gdi\drawcaption.htm
tech.root: gdi
ms.assetid: 9348e29f-ce56-4664-8862-f5810c797622
ms.date: 12/05/2018
ms.keywords: DC_ACTIVE, DC_BUTTONS, DC_GRADIENT, DC_ICON, DC_INBUTTON, DC_SMALLCAP, DC_TEXT, DrawCaption, DrawCaption function [Windows GDI], _win32_DrawCaption, gdi.drawcaption, winuser/DrawCaption
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawCaption
 - winuser/DrawCaption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
api_name:
 - DrawCaption
---

# DrawCaption function


## -description

The <b>DrawCaption</b> function draws a window caption.

## -parameters

### -param hwnd [in]

A handle to a window that supplies text and an icon for the window caption.

### -param hdc [in]

A handle to a device context. The function draws the window caption into this device context.

### -param lprect [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the bounding rectangle for the window caption in logical coordinates.

### -param flags [in]

The drawing options. This parameter can be zero or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DC_ACTIVE"></a><a id="dc_active"></a><dl>
<dt><b>DC_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The function uses the colors that denote an active caption.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_BUTTONS"></a><a id="dc_buttons"></a><dl>
<dt><b>DC_BUTTONS</b></dt>
</dl>
</td>
<td width="60%">
If set, the function draws the buttons in the caption bar (to minimize, restore, or close an application).

</td>
</tr>
<tr>
<td width="40%"><a id="DC_GRADIENT"></a><a id="dc_gradient"></a><dl>
<dt><b>DC_GRADIENT</b></dt>
</dl>
</td>
<td width="60%">
When this flag is set, the function uses COLOR_GRADIENTACTIVECAPTION (if the DC_ACTIVE flag was set) or COLOR_GRADIENTINACTIVECAPTION for the title-bar color.

If this flag is not set, the function uses COLOR_ACTIVECAPTION or COLOR_INACTIVECAPTION for both colors.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_ICON"></a><a id="dc_icon"></a><dl>
<dt><b>DC_ICON</b></dt>
</dl>
</td>
<td width="60%">
The function draws the icon when drawing the caption text.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_INBUTTON"></a><a id="dc_inbutton"></a><dl>
<dt><b>DC_INBUTTON</b></dt>
</dl>
</td>
<td width="60%">
The function draws the caption as a button.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_SMALLCAP"></a><a id="dc_smallcap"></a><dl>
<dt><b>DC_SMALLCAP</b></dt>
</dl>
</td>
<td width="60%">
The function draws a small caption, using the current small caption font.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_TEXT"></a><a id="dc_text"></a><dl>
<dt><b>DC_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The function draws the caption text when drawing the caption.

</td>
</tr>
</table>
 

If DC_SMALLCAP is specified, the function draws a normal window caption.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>