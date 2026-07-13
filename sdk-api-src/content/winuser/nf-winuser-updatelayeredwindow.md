---
UID: NF:winuser.UpdateLayeredWindow
title: UpdateLayeredWindow function (winuser.h)
description: Updates the position, size, shape, content, and translucency of a layered window.
helpviewer_keywords: ["ULW_ALPHA","ULW_COLORKEY","ULW_EX_NORESIZE","ULW_OPAQUE","UpdateLayeredWindow","UpdateLayeredWindow function [Windows and Messages]","_win32_UpdateLayeredWindow","_win32_updatelayeredwindow_cpp","winmsg.updatelayeredwindow","winui._win32_updatelayeredwindow","winuser/UpdateLayeredWindow"]
old-location: winmsg\updatelayeredwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\updatelayeredwindow.htm
ms.date: 12/05/2018
ms.keywords: ULW_ALPHA, ULW_COLORKEY, ULW_EX_NORESIZE, ULW_OPAQUE, UpdateLayeredWindow, UpdateLayeredWindow function [Windows and Messages], _win32_UpdateLayeredWindow, _win32_updatelayeredwindow_cpp, winmsg.updatelayeredwindow, winui._win32_updatelayeredwindow, winuser/UpdateLayeredWindow
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
 - UpdateLayeredWindow
 - winuser/UpdateLayeredWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - UpdateLayeredWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-1 (introduced in Windows 8.1)
---

# UpdateLayeredWindow function


## -description

Updates the position, size, shape, content, and translucency of a layered window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to a layered window. A layered window is created by specifying <b>WS_EX_LAYERED</b> when creating the window with the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function. 

<b>Windows 8:  </b>The <b>WS_EX_LAYERED</b> style is supported for top-level windows and child windows. Previous Windows versions support <b>WS_EX_LAYERED</b> only for top-level windows.

### -param hdcDst [in, optional]

Type: <b>HDC</b>

A handle to a DC for the screen. This handle is obtained by specifying <b>NULL</b> when calling the <a href="/windows/win32/api/winuser/nf-winuser-getdc">GetDC</a> function. It is used for palette color matching when the window contents are updated. If <i>hdcDst</i> is <b>NULL</b>, the default palette will be used.

If <i>hdcSrc</i> is <b>NULL</b>, <i>hdcDst</i> must be <b>NULL</b>.

### -param pptDst [in, optional]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A pointer to a structure that specifies the new screen position of the layered window. If the current position is not changing, <i>pptDst</i> can be <b>NULL</b>.

### -param psize [in, optional]

Type: <b><a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>*</b>

A pointer to a structure that specifies the new size of the layered window. If the size of the window is not changing, <i>psize</i> can be <b>NULL</b>. If <i>hdcSrc</i> is <b>NULL</b>, <i>psize</i> must be <b>NULL</b>.

### -param hdcSrc [in, optional]

Type: <b>HDC</b>

A handle to a DC for the surface that defines the layered window. This handle can be obtained by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc">CreateCompatibleDC</a> function. If the shape and visual context of the window are not changing, <i>hdcSrc</i> can be <b>NULL</b>.

### -param pptSrc [in, optional]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A pointer to a structure that specifies the location of the layer in the device context. If <i>hdcSrc</i> is <b>NULL</b>, <i>pptSrc</i> should be <b>NULL</b>.

### -param crKey [in]

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

A structure that specifies the color key to be used when composing the layered window. To generate a <a href="/windows/desktop/gdi/colorref">COLORREF</a>, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

### -param pblend [in, optional]

Type: <b><a href="/windows/desktop/api/wingdi/ns-wingdi-blendfunction">BLENDFUNCTION</a>*</b>

A pointer to a structure that specifies the transparency value to be used when composing the layered window.

### -param dwFlags [in]

Type: <b>DWORD</b>

This parameter can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ULW_ALPHA"></a><a id="ulw_alpha"></a><dl>
<dt><b>ULW_ALPHA</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Use <i>pblend</i> as the blend function. If the display mode is 256 colors or less, the effect of this value is the same as the effect of <b>ULW_OPAQUE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="ULW_COLORKEY"></a><a id="ulw_colorkey"></a><dl>
<dt><b>ULW_COLORKEY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Use <i>crKey</i> as the transparency color. 

</td>
</tr>
<tr>
<td width="40%"><a id="ULW_OPAQUE"></a><a id="ulw_opaque"></a><dl>
<dt><b>ULW_OPAQUE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Draw an opaque layered window. 

</td>
</tr>
<tr>
<td width="40%"><a id="ULW_EX_NORESIZE"></a><a id="ulw_ex_noresize"></a><dl>
<dt><b>ULW_EX_NORESIZE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Force the <a href="/previous-versions/windows/desktop/legacy/ms633557(v=vs.85)">UpdateLayeredWindowIndirect</a> function to fail if the current window size does not match the size specified in the <i>psize</i>. 

</td>
</tr>
</table>
 

If <i>hdcSrc</i> is <b>NULL</b>, <i>dwFlags</i> should be zero.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The source DC should contain the surface that defines the visible contents of the layered window. For example, you can select a bitmap into a device context obtained by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc">CreateCompatibleDC</a> function. 

An application should call <a href="/windows/desktop/api/wingdi/nf-wingdi-setlayout">SetLayout</a> on the <i>hdcSrc</i> device context to properly set the mirroring mode. <b>SetLayout</b> will properly mirror all drawing into an <b>HDC</b> while properly preserving text glyph and (optionally) bitmap direction order. It cannot modify drawing directly into the bits of a device-independent bitmap (DIB). For more information, see <a href="/windows/desktop/winmsg/window-features">Window Layout and Mirroring</a>.

The <b>UpdateLayeredWindow</b> function maintains the window's appearance on the screen. The windows underneath a layered window do not need to be repainted when they are uncovered due to a call to <b>UpdateLayeredWindow</b>, because the system will automatically repaint them. This permits seamless animation of the layered window. 

<b>UpdateLayeredWindow</b> always updates the entire window. To update part of a window, use the traditional <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> and set the blend value using <a href="/windows/desktop/api/winuser/nf-winuser-setlayeredwindowattributes">SetLayeredWindowAttributes</a>.

For best drawing performance by the layered window and any underlying windows, the layered window should be as small as possible. An application should also process the  message and re-create its layered windows when the display's color depth changes.

For more information, see <a href="/windows/desktop/winmsg/window-features">Layered Windows</a>.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-alphablend">AlphaBlend</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap">CreateCompatibleBitmap</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga">SetWindowLong</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowpos">SetWindowPos</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-transparentblt">TransparentBlt</a>



<a href="/previous-versions/windows/desktop/legacy/ms633557(v=vs.85)">UpdateLayeredWindowIndirect</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
