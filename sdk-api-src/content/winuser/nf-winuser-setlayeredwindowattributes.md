---
UID: NF:winuser.SetLayeredWindowAttributes
title: SetLayeredWindowAttributes function (winuser.h)
description: Sets the opacity and transparency color key of a layered window.
helpviewer_keywords: ["LWA_ALPHA","LWA_COLORKEY","SetLayeredWindowAttributes","SetLayeredWindowAttributes function [Windows and Messages]","_win32_SetLayeredWindowAttributes","_win32_setlayeredwindowattributes_cpp","winmsg.setlayeredwindowattributes","winui._win32_setlayeredwindowattributes","winuser/SetLayeredWindowAttributes"]
old-location: winmsg\setlayeredwindowattributes.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\setlayeredwindowattributes.htm
ms.date: 12/05/2018
ms.keywords: LWA_ALPHA, LWA_COLORKEY, SetLayeredWindowAttributes, SetLayeredWindowAttributes function [Windows and Messages], _win32_SetLayeredWindowAttributes, _win32_setlayeredwindowattributes_cpp, winmsg.setlayeredwindowattributes, winui._win32_setlayeredwindowattributes, winuser/SetLayeredWindowAttributes
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
 - SetLayeredWindowAttributes
 - winuser/SetLayeredWindowAttributes
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
 - Ext-MS-Win-NTUser-Window-L1-1-0.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SetLayeredWindowAttributes
req.apiset: ext-ms-win-ntuser-window-l1-1-1 (introduced in Windows 8.1)
---

# SetLayeredWindowAttributes function


## -description

Sets the opacity and transparency color key of a layered window.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the layered window. A layered window is created by specifying <b>WS_EX_LAYERED</b> when creating the window with the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function or by setting <b>WS_EX_LAYERED</b> via <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga">SetWindowLong</a> after the window has been created.

<b>Windows 8:  </b>The <b>WS_EX_LAYERED</b> style is supported for top-level windows and child windows. Previous Windows versions support <b>WS_EX_LAYERED</b> only for top-level windows.

### -param crKey [in]

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

A <a href="/windows/desktop/gdi/colorref">COLORREF</a> structure that specifies the transparency color key to be used when composing the layered window. All pixels painted by the window in this color will be transparent. To generate a <b>COLORREF</b>, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

### -param bAlpha [in]

Type: <b>BYTE</b>

Alpha value used to describe the opacity of the layered window. Similar to the <b>SourceConstantAlpha</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-blendfunction">BLENDFUNCTION</a> structure. When <i>bAlpha</i> is 0, the window is completely transparent. When <i>bAlpha</i> is 255, the window is opaque.

### -param dwFlags [in]

Type: <b>DWORD</b>

An action to be taken. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LWA_ALPHA"></a><a id="lwa_alpha"></a><dl>
<dt><b>LWA_ALPHA</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Use <i>bAlpha</i> to determine the opacity of the layered window.

</td>
</tr>
<tr>
<td width="40%"><a id="LWA_COLORKEY"></a><a id="lwa_colorkey"></a><dl>
<dt><b>LWA_COLORKEY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Use <i>crKey</i> as the transparency color.

</td>
</tr>
</table>

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

                    

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Note that once <b>SetLayeredWindowAttributes</b> has been called for a layered window, subsequent <a href="/windows/desktop/api/winuser/nf-winuser-updatelayeredwindow">UpdateLayeredWindow</a> calls will fail until the layering style bit is cleared and set again.

For more information, see <a href="/windows/desktop/winmsg/using-windows">Using Layered Windows</a>.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-alphablend">AlphaBlend</a>



<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga">SetWindowLong</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-transparentblt">TransparentBlt</a>



<a href="/windows/desktop/api/winuser/nf-winuser-updatelayeredwindow">UpdateLayeredWindow</a>



<a href="/windows/desktop/winmsg/using-windows">Using Windows</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
