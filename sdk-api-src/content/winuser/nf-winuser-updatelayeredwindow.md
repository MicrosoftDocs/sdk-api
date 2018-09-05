---
UID: NF:winuser.UpdateLayeredWindow
title: UpdateLayeredWindow function
author: windows-sdk-content
description: Updates the position, size, shape, content, and translucency of a layered window.
old-location: winmsg\updatelayeredwindow.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\updatelayeredwindow.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ULW_ALPHA, ULW_COLORKEY, ULW_OPAQUE, UpdateLayeredWindow, UpdateLayeredWindow function [Windows and Messages], _win32_UpdateLayeredWindow, _win32_updatelayeredwindow_cpp, winmsg.updatelayeredwindow, winui._win32_updatelayeredwindow, winuser/UpdateLayeredWindow
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - UpdateLayeredWindow
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# UpdateLayeredWindow function


## -description


Updates the position, size, shape, content, and translucency of a layered window. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to a layered window. A layered window is created by specifying <b>WS_EX_LAYERED</b> when creating the window with the <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function. 

<b>Windows 8:  </b>The <b>WS_EX_LAYERED</b> style is supported for top-level windows and child windows. Previous Windows versions support <b>WS_EX_LAYERED</b> only for top-level windows.


### -param hdcDst [in, optional]

Type: <b>HDC</b>

A handle to a DC for the screen. This handle is obtained by specifying <b>NULL</b> when calling the  function. It is used for palette color matching when the window contents are updated. If <i>hdcDst</i> is<b>NULL</b>, the default palette will be used.

If <i>hdcSrc</i> is <b>NULL</b>, <i>hdcDst</i> must be <b>NULL</b>.


### -param pptDst [in, optional]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

A pointer to a structure that specifies the new screen position of the layered window. If the current position is not changing, <i>pptDst</i> can be <b>NULL</b>. 


### -param psize [in, optional]

Type: <b><a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>*</b>

A pointer to a structure that specifies the new size of the layered window. If the size of the window is not changing, <i>psize</i> can be <b>NULL</b>. If <i>hdcSrc</i> is <b>NULL</b>, <i>psize</i> must be <b>NULL</b>. 


### -param hdcSrc [in, optional]

Type: <b>HDC</b>

A handle to a DC for the surface that defines the layered window. This handle can be obtained by calling the <a href="https://msdn.microsoft.com/6ddc3705-2995-41af-af94-258aed597e17">CreateCompatibleDC</a> function. If the shape and visual context of the window are not changing, <i>hdcSrc</i> can be <b>NULL</b>. 


### -param pptSrc [in, optional]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

A pointer to a structure that specifies the location of the layer in the device context. If <i>hdcSrc</i> is <b>NULL</b>, <i>pptSrc</i> should be <b>NULL</b>. 


### -param crKey [in]

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

A structure that specifies the color key to be used when composing the layered window. To generate a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro. 


### -param pblend [in, optional]

Type: <b><a href="https://msdn.microsoft.com/d1371d72-c408-4484-845e-d4ea2bc3115d">BLENDFUNCTION</a>*</b>

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
</table>
 

If <i>hdcSrc</i> is <b>NULL</b>, <i>dwFlags</i> should be zero.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The source DC should contain the surface that defines the visible contents of the layered window. For example, you can select a bitmap into a device context obtained by calling the <a href="https://msdn.microsoft.com/6ddc3705-2995-41af-af94-258aed597e17">CreateCompatibleDC</a> function. 

An application should call <a href="https://msdn.microsoft.com/81c6dccd-cfb1-486f-8c25-f46ba7c3ff8d">SetLayout</a> on the <i>hdcSrc</i> device context to properly set the mirroring mode. <b>SetLayout</b> will properly mirror all drawing into an <b>HDC</b> while properly preserving text glyph and (optionally) bitmap direction order. It cannot modify drawing directly into the bits of a device-independent bitmap (DIB). For more information, see <a href="window_features.htm">Window Layout and Mirroring</a>.

The <b>UpdateLayeredWindow</b> function maintains the window's appearance on the screen. The windows underneath a layered window do not need to be repainted when they are uncovered due to a call to <b>UpdateLayeredWindow</b>, because the system will automatically repaint them. This permits seamless animation of the layered window. 

<b>UpdateLayeredWindow</b> always updates the entire window. To update part of a window, use the traditional <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> and set the blend value using <a href="https://msdn.microsoft.com/5654fa0c-33cf-4014-9d75-0d512fdffacd">SetLayeredWindowAttributes</a>.

For best drawing performance by the layered window and any underlying windows, the layered window should be as small as possible. An application should also process the  message and re-create its layered windows when the display's color depth changes.

For more information, see <a href="window_features.htm">Layered Windows</a>. 




## -see-also




<a href="https://msdn.microsoft.com/4624aa31-7e19-4506-ac70-9b3c98a8215d">AlphaBlend</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d2866beb-ff7a-4390-8651-e7bf458ddf88">CreateCompatibleBitmap</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/75f6721f-188c-4daa-9410-6cb2d86869fc">SetWindowLong</a>



<a href="https://msdn.microsoft.com/e0a28590-0fed-4ffa-adcd-84b60df316b5">SetWindowPos</a>



<a href="https://msdn.microsoft.com/900b2ca3-398d-4128-a1ae-8b4940574327">TransparentBlt</a>



<a href="https://msdn.microsoft.com/151fe26d-e5cd-43fd-9b33-5f08e06ca443">UpdateLayeredWindowIndirect</a>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

