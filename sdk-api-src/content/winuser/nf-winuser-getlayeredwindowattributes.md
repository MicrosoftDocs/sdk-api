---
UID: NF:winuser.GetLayeredWindowAttributes
title: GetLayeredWindowAttributes function (winuser.h)
description: Retrieves the opacity and transparency color key of a layered window.
helpviewer_keywords: ["GetLayeredWindowAttributes","GetLayeredWindowAttributes function [Windows and Messages]","LWA_ALPHA","LWA_COLORKEY","_win32_GetLayeredWindowAttributes","_win32_getlayeredwindowattributes_cpp","winmsg.getlayeredwindowattributes","winui._win32_getlayeredwindowattributes","winuser/GetLayeredWindowAttributes"]
old-location: winmsg\getlayeredwindowattributes.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getlayeredwindowattributes.htm
ms.date: 12/05/2018
ms.keywords: GetLayeredWindowAttributes, GetLayeredWindowAttributes function [Windows and Messages], LWA_ALPHA, LWA_COLORKEY, _win32_GetLayeredWindowAttributes, _win32_getlayeredwindowattributes_cpp, winmsg.getlayeredwindowattributes, winui._win32_getlayeredwindowattributes, winuser/GetLayeredWindowAttributes
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetLayeredWindowAttributes
 - winuser/GetLayeredWindowAttributes
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
 - GetLayeredWindowAttributes
req.apiset: ext-ms-win-ntuser-window-l1-1-1 (introduced in Windows 8.1)
---

# GetLayeredWindowAttributes function


## -description

Retrieves the opacity and transparency color key of a layered window.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the layered window. A layered window is created by specifying <b>WS_EX_LAYERED</b> when creating the window with the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function or by setting <b>WS_EX_LAYERED</b> using <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga">SetWindowLong</a> after the window has been created.

### -param pcrKey [out, optional]

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a>*</b>

A pointer to a <a href="/windows/desktop/gdi/colorref">COLORREF</a> value that receives the transparency color key to be used when composing the layered window. All pixels painted by the window in this color will be transparent. This can be <b>NULL</b> if the argument is not needed.

### -param pbAlpha [out, optional]

Type: <b>BYTE*</b>

The Alpha value used to describe the opacity of the layered window. Similar to the <b>SourceConstantAlpha</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-blendfunction">BLENDFUNCTION</a> structure. When the variable referred to by <i>pbAlpha</i> is 0, the window is completely transparent. When the variable referred to by <i>pbAlpha</i> is 255, the window is opaque. This can be <b>NULL</b> if the argument is not needed.

### -param pdwFlags [out, optional]

Type: <b>DWORD*</b>

A layering flag. This parameter can be <b>NULL</b> if the value is not needed. The layering flag can be one or more of the following values.

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
Use <i>pbAlpha</i> to determine the opacity of the layered window.

</td>
</tr>
<tr>
<td width="40%"><a id="LWA_COLORKEY"></a><a id="lwa_colorkey"></a><dl>
<dt><b>LWA_COLORKEY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Use <i>pcrKey</i> as the transparency color. 

</td>
</tr>
</table>

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>GetLayeredWindowAttributes</b> can be called only if the application has previously called <a href="/windows/desktop/api/winuser/nf-winuser-setlayeredwindowattributes">SetLayeredWindowAttributes</a> on the window. The function will fail if the layered window was setup with <a href="/windows/desktop/api/winuser/nf-winuser-updatelayeredwindow">UpdateLayeredWindow</a>.

For more information, see <a href="/windows/desktop/winmsg/using-windows">Using Layered Windows</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setlayeredwindowattributes">SetLayeredWindowAttributes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga">SetWindowLong</a>



<a href="/windows/desktop/winmsg/using-windows">Using Windows</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
