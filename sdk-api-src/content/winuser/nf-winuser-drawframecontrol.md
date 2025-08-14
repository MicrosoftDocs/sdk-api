---
UID: NF:winuser.DrawFrameControl
title: DrawFrameControl function (winuser.h)
description: The DrawFrameControl function draws a frame control of the specified type and style.
helpviewer_keywords: ["DFCS_ADJUSTRECT","DFCS_BUTTON3STATE","DFCS_BUTTONCHECK","DFCS_BUTTONPUSH","DFCS_BUTTONRADIO","DFCS_BUTTONRADIOIMAGE","DFCS_BUTTONRADIOMASK","DFCS_CAPTIONCLOSE","DFCS_CAPTIONHELP","DFCS_CAPTIONMAX","DFCS_CAPTIONMIN","DFCS_CAPTIONRESTORE","DFCS_CHECKED","DFCS_FLAT","DFCS_HOT","DFCS_INACTIVE","DFCS_MENUARROW","DFCS_MENUARROWRIGHT","DFCS_MENUBULLET","DFCS_MENUCHECK","DFCS_MONO","DFCS_PUSHED","DFCS_SCROLLCOMBOBOX","DFCS_SCROLLDOWN","DFCS_SCROLLLEFT","DFCS_SCROLLRIGHT","DFCS_SCROLLSIZEGRIP","DFCS_SCROLLSIZEGRIPRIGHT","DFCS_SCROLLUP","DFCS_TRANSPARENT","DFC_BUTTON","DFC_CAPTION","DFC_MENU","DFC_POPUPMENU","DFC_SCROLL","DrawFrameControl","DrawFrameControl function [Windows GDI]","_win32_DrawFrameControl","gdi.drawframecontrol","winuser/DrawFrameControl"]
old-location: gdi\drawframecontrol.htm
tech.root: gdi
ms.assetid: 3102007e-e9f7-46d8-ae10-cf156d2131f6
ms.date: 12/05/2018
ms.keywords: DFCS_ADJUSTRECT, DFCS_BUTTON3STATE, DFCS_BUTTONCHECK, DFCS_BUTTONPUSH, DFCS_BUTTONRADIO, DFCS_BUTTONRADIOIMAGE, DFCS_BUTTONRADIOMASK, DFCS_CAPTIONCLOSE, DFCS_CAPTIONHELP, DFCS_CAPTIONMAX, DFCS_CAPTIONMIN, DFCS_CAPTIONRESTORE, DFCS_CHECKED, DFCS_FLAT, DFCS_HOT, DFCS_INACTIVE, DFCS_MENUARROW, DFCS_MENUARROWRIGHT, DFCS_MENUBULLET, DFCS_MENUCHECK, DFCS_MONO, DFCS_PUSHED, DFCS_SCROLLCOMBOBOX, DFCS_SCROLLDOWN, DFCS_SCROLLLEFT, DFCS_SCROLLRIGHT, DFCS_SCROLLSIZEGRIP, DFCS_SCROLLSIZEGRIPRIGHT, DFCS_SCROLLUP, DFCS_TRANSPARENT, DFC_BUTTON, DFC_CAPTION, DFC_MENU, DFC_POPUPMENU, DFC_SCROLL, DrawFrameControl, DrawFrameControl function [Windows GDI], _win32_DrawFrameControl, gdi.drawframecontrol, winuser/DrawFrameControl
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
 - DrawFrameControl
 - winuser/DrawFrameControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-draw-l1-1-0.dll
 - user32.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
 - DrawFrameControl
req.apiset: ext-ms-win-ntuser-draw-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

## -description

The <b>DrawFrameControl</b> function draws a frame control of the specified type and style.

## -parameters

### -param hdc [in]

A handle to the device context of the window in which to draw the control.

### -param lprc [in]

 A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the logical coordinates of the bounding rectangle for frame control.

### -param uType [in]

The type of frame control to draw. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DFC_BUTTON"></a><a id="dfc_button"></a><dl>
<dt><b>DFC_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
Standard button

</td>
</tr>
<tr>
<td width="40%"><a id="DFC_CAPTION"></a><a id="dfc_caption"></a><dl>
<dt><b>DFC_CAPTION</b></dt>
</dl>
</td>
<td width="60%">
Title bar

</td>
</tr>
<tr>
<td width="40%"><a id="DFC_MENU"></a><a id="dfc_menu"></a><dl>
<dt><b>DFC_MENU</b></dt>
</dl>
</td>
<td width="60%">
Menu bar

</td>
</tr>
<tr>
<td width="40%"><a id="DFC_POPUPMENU"></a><a id="dfc_popupmenu"></a><dl>
<dt><b>DFC_POPUPMENU</b></dt>
</dl>
</td>
<td width="60%">
Popup menu item.

</td>
</tr>
<tr>
<td width="40%"><a id="DFC_SCROLL"></a><a id="dfc_scroll"></a><dl>
<dt><b>DFC_SCROLL</b></dt>
</dl>
</td>
<td width="60%">
Scroll bar

</td>
</tr>
</table>

### -param uState [in]

The initial state of the frame control. If <i>uType</i> is DFC_BUTTON, <i>uState</i> can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DFCS_BUTTON3STATE"></a><a id="dfcs_button3state"></a><dl>
<dt><b>DFCS_BUTTON3STATE</b></dt>
</dl>
</td>
<td width="60%">
Three-state button

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_BUTTONCHECK"></a><a id="dfcs_buttoncheck"></a><dl>
<dt><b>DFCS_BUTTONCHECK</b></dt>
</dl>
</td>
<td width="60%">
Check box

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_BUTTONPUSH"></a><a id="dfcs_buttonpush"></a><dl>
<dt><b>DFCS_BUTTONPUSH</b></dt>
</dl>
</td>
<td width="60%">
Push button

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_BUTTONRADIO"></a><a id="dfcs_buttonradio"></a><dl>
<dt><b>DFCS_BUTTONRADIO</b></dt>
</dl>
</td>
<td width="60%">
Radio button

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_BUTTONRADIOIMAGE"></a><a id="dfcs_buttonradioimage"></a><dl>
<dt><b>DFCS_BUTTONRADIOIMAGE</b></dt>
</dl>
</td>
<td width="60%">
Image for radio button (nonsquare needs image)

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_BUTTONRADIOMASK"></a><a id="dfcs_buttonradiomask"></a><dl>
<dt><b>DFCS_BUTTONRADIOMASK</b></dt>
</dl>
</td>
<td width="60%">
Mask for radio button (nonsquare needs mask)

</td>
</tr>
</table>
 

If <i>uType</i> is DFC_CAPTION, <i>uState</i> can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DFCS_CAPTIONCLOSE"></a><a id="dfcs_captionclose"></a><dl>
<dt><b>DFCS_CAPTIONCLOSE</b></dt>
</dl>
</td>
<td width="60%">
<b>Close</b> button

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_CAPTIONHELP"></a><a id="dfcs_captionhelp"></a><dl>
<dt><b>DFCS_CAPTIONHELP</b></dt>
</dl>
</td>
<td width="60%">
<b>Help</b> button

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_CAPTIONMAX"></a><a id="dfcs_captionmax"></a><dl>
<dt><b>DFCS_CAPTIONMAX</b></dt>
</dl>
</td>
<td width="60%">
<b>Maximize</b> button

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_CAPTIONMIN"></a><a id="dfcs_captionmin"></a><dl>
<dt><b>DFCS_CAPTIONMIN</b></dt>
</dl>
</td>
<td width="60%">
<b>Minimize</b> button

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_CAPTIONRESTORE"></a><a id="dfcs_captionrestore"></a><dl>
<dt><b>DFCS_CAPTIONRESTORE</b></dt>
</dl>
</td>
<td width="60%">
<b>Restore</b> button

</td>
</tr>
</table>
 

If <i>uType</i> is DFC_MENU, <i>uState</i> can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DFCS_MENUARROW"></a><a id="dfcs_menuarrow"></a><dl>
<dt><b>DFCS_MENUARROW</b></dt>
</dl>
</td>
<td width="60%">
Submenu arrow

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_MENUARROWRIGHT"></a><a id="dfcs_menuarrowright"></a><dl>
<dt><b>DFCS_MENUARROWRIGHT</b></dt>
</dl>
</td>
<td width="60%">
Submenu arrow pointing left. This is used for the right-to-left cascading menus used with right-to-left languages such as Arabic or Hebrew.

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_MENUBULLET"></a><a id="dfcs_menubullet"></a><dl>
<dt><b>DFCS_MENUBULLET</b></dt>
</dl>
</td>
<td width="60%">
Bullet

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_MENUCHECK"></a><a id="dfcs_menucheck"></a><dl>
<dt><b>DFCS_MENUCHECK</b></dt>
</dl>
</td>
<td width="60%">
Check mark

</td>
</tr>
</table>
 

If <i>uType</i> is DFC_SCROLL, <i>uState</i> can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DFCS_SCROLLCOMBOBOX"></a><a id="dfcs_scrollcombobox"></a><dl>
<dt><b>DFCS_SCROLLCOMBOBOX</b></dt>
</dl>
</td>
<td width="60%">
Combo box scroll bar

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_SCROLLDOWN"></a><a id="dfcs_scrolldown"></a><dl>
<dt><b>DFCS_SCROLLDOWN</b></dt>
</dl>
</td>
<td width="60%">
Down arrow of scroll bar

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_SCROLLLEFT"></a><a id="dfcs_scrollleft"></a><dl>
<dt><b>DFCS_SCROLLLEFT</b></dt>
</dl>
</td>
<td width="60%">
Left arrow of scroll bar

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_SCROLLRIGHT"></a><a id="dfcs_scrollright"></a><dl>
<dt><b>DFCS_SCROLLRIGHT</b></dt>
</dl>
</td>
<td width="60%">
Right arrow of scroll bar

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_SCROLLSIZEGRIP"></a><a id="dfcs_scrollsizegrip"></a><dl>
<dt><b>DFCS_SCROLLSIZEGRIP</b></dt>
</dl>
</td>
<td width="60%">
Size grip in lower-right corner of window

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_SCROLLSIZEGRIPRIGHT"></a><a id="dfcs_scrollsizegripright"></a><dl>
<dt><b>DFCS_SCROLLSIZEGRIPRIGHT</b></dt>
</dl>
</td>
<td width="60%">
Size grip in lower-left corner of window. This is used with right-to-left languages such as Arabic or Hebrew.

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_SCROLLUP"></a><a id="dfcs_scrollup"></a><dl>
<dt><b>DFCS_SCROLLUP</b></dt>
</dl>
</td>
<td width="60%">
Up arrow of scroll bar

</td>
</tr>
</table>
 

The following style can be used to adjust the bounding rectangle of the push button.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DFCS_ADJUSTRECT"></a><a id="dfcs_adjustrect"></a><dl>
<dt><b>DFCS_ADJUSTRECT</b></dt>
</dl>
</td>
<td width="60%">
Bounding rectangle is adjusted to exclude the surrounding edge of the push button.

</td>
</tr>
</table>
 

One or more of the following values can be used to set the state of the control to be drawn.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DFCS_CHECKED"></a><a id="dfcs_checked"></a><dl>
<dt><b>DFCS_CHECKED</b></dt>
</dl>
</td>
<td width="60%">
Button is checked.

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_FLAT"></a><a id="dfcs_flat"></a><dl>
<dt><b>DFCS_FLAT</b></dt>
</dl>
</td>
<td width="60%">
Button has a flat border.

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_HOT"></a><a id="dfcs_hot"></a><dl>
<dt><b>DFCS_HOT</b></dt>
</dl>
</td>
<td width="60%">
Button is hot-tracked.

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_INACTIVE"></a><a id="dfcs_inactive"></a><dl>
<dt><b>DFCS_INACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Button is inactive (grayed).

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_MONO"></a><a id="dfcs_mono"></a><dl>
<dt><b>DFCS_MONO</b></dt>
</dl>
</td>
<td width="60%">
Button has a monochrome border.

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_PUSHED"></a><a id="dfcs_pushed"></a><dl>
<dt><b>DFCS_PUSHED</b></dt>
</dl>
</td>
<td width="60%">
Button is pushed.

</td>
</tr>
<tr>
<td width="40%"><a id="DFCS_TRANSPARENT"></a><a id="dfcs_transparent"></a><dl>
<dt><b>DFCS_TRANSPARENT</b></dt>
</dl>
</td>
<td width="60%">
The background remains untouched. This flag can only be combined with DFCS_MENUARROWUP or DFCS_MENUARROWDOWN.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

If <i>uType</i> is either DFC_MENU or DFC_BUTTON and <i>uState</i> is not DFCS_BUTTONPUSH, the frame control is a black-on-white mask (that is, a black frame control on a white background). In such cases, the application must pass a handle to a bitmap memory device control. The application can then use the associated bitmap as the <i>hbmMask</i> parameter to the <a href="/windows/desktop/api/wingdi/nf-wingdi-maskblt">MaskBlt</a> function, or it can use the device context as a parameter to the <a href="/windows/desktop/api/wingdi/nf-wingdi-bitblt">BitBlt</a> function using ROPs such as SRCAND and SRCINVERT.

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The input given is always in terms of physical pixels, and is not related to the calling context.

## -see-also

<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT
      </a>
