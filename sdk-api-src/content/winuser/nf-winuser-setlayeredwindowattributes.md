---
UID: NF:winuser.SetLayeredWindowAttributes
title: SetLayeredWindowAttributes function
author: windows-sdk-content
description: Sets the opacity and transparency color key of a layered window.
old-location: winmsg\setlayeredwindowattributes.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\setlayeredwindowattributes.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: LWA_ALPHA, LWA_COLORKEY, SetLayeredWindowAttributes, SetLayeredWindowAttributes function [Windows and Messages], _win32_SetLayeredWindowAttributes, _win32_setlayeredwindowattributes_cpp, winmsg.setlayeredwindowattributes, winui._win32_setlayeredwindowattributes, winuser/SetLayeredWindowAttributes
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
 - Ext-MS-Win-NTUser-Window-L1-1-0.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SetLayeredWindowAttributes
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetLayeredWindowAttributes function


## -description


Sets the opacity and transparency color key of a layered window.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the layered window. A layered window is created by specifying <b>WS_EX_LAYERED</b> when creating the window with the <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function or by setting <b>WS_EX_LAYERED</b> via <a href="https://msdn.microsoft.com/75f6721f-188c-4daa-9410-6cb2d86869fc">SetWindowLong</a> after the window has been created.

<b>Windows 8:  </b>The <b>WS_EX_LAYERED</b> style is supported for top-level windows and child windows. Previous Windows versions support <b>WS_EX_LAYERED</b> only for top-level windows.


### -param crKey [in]

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

A <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> structure that specifies the transparency color key to be used when composing the layered window. All pixels painted by the window in this color will be transparent. To generate a <b>COLORREF</b>, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


### -param bAlpha [in]

Type: <b>BYTE</b>

Alpha value used to describe the opacity of the layered window. Similar to the <b>SourceConstantAlpha</b> member of the <a href="https://msdn.microsoft.com/d1371d72-c408-4484-845e-d4ea2bc3115d">BLENDFUNCTION</a> structure. When <i>bAlpha</i> is 0, the window is completely transparent. When <i>bAlpha</i> is 255, the window is opaque.


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



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

                    

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Note that once <b>SetLayeredWindowAttributes</b> has been called for a layered window, subsequent <a href="https://msdn.microsoft.com/3f4a3608-2383-46d5-b1b2-53a939bf736a">UpdateLayeredWindow</a> calls will fail until the layering style bit is cleared and set again.

For more information, see <a href="using_windows.htm">Using Layered Windows</a>.




## -see-also




<a href="https://msdn.microsoft.com/4624aa31-7e19-4506-ac70-9b3c98a8215d">AlphaBlend</a>



<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/75f6721f-188c-4daa-9410-6cb2d86869fc">SetWindowLong</a>



<a href="https://msdn.microsoft.com/900b2ca3-398d-4128-a1ae-8b4940574327">TransparentBlt</a>



<a href="https://msdn.microsoft.com/3f4a3608-2383-46d5-b1b2-53a939bf736a">UpdateLayeredWindow</a>



<a href="https://msdn.microsoft.com/7695fb64-3918-4d9a-8cd8-01d20edd9c55">Using Windows</a>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

