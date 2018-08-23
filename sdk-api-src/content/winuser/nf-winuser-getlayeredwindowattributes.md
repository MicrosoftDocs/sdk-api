---
UID: NF:winuser.GetLayeredWindowAttributes
title: GetLayeredWindowAttributes function
author: windows-sdk-content
description: Retrieves the opacity and transparency color key of a layered window.
old-location: winmsg\getlayeredwindowattributes.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getlayeredwindowattributes.htm
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: GetLayeredWindowAttributes, GetLayeredWindowAttributes function [Windows and Messages], LWA_ALPHA, LWA_COLORKEY, _win32_GetLayeredWindowAttributes, _win32_getlayeredwindowattributes_cpp, winmsg.getlayeredwindowattributes, winui._win32_getlayeredwindowattributes, winuser/GetLayeredWindowAttributes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
 - GetLayeredWindowAttributes
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetLayeredWindowAttributes function


## -description


Retrieves the opacity and transparency color key of a layered window.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the layered window. A layered window is created by specifying <b>WS_EX_LAYERED</b> when creating the window with the <a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a> function or by setting <b>WS_EX_LAYERED</b> using <a href="https://msdn.microsoft.com/en-us/library/ms633591(v=VS.85).aspx">SetWindowLong</a> after the window has been created. 


### -param pcrKey [out, optional]

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value that receives the transparency color key to be used when composing the layered window. All pixels painted by the window in this color will be transparent. This can be <b>NULL</b> if the argument is not needed. 


### -param pbAlpha [out, optional]

Type: <b>BYTE*</b>

The Alpha value used to describe the opacity of the layered window. Similar to the <b>SourceConstantAlpha</b> member of the <a href="https://msdn.microsoft.com/d1371d72-c408-4484-845e-d4ea2bc3115d">BLENDFUNCTION</a> structure. When the variable referred to by <i>pbAlpha</i> is 0, the window is completely transparent. When the variable referred to by <i>pbAlpha</i> is 255, the window is opaque. This can be <b>NULL</b> if the argument is not needed. 


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



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<b>GetLayeredWindowAttributes</b> can be called only if the application has previously called <a href="https://msdn.microsoft.com/en-us/library/ms633540(v=VS.85).aspx">SetLayeredWindowAttributes</a> on the window. The function will fail if the layered window was setup with <a href="https://msdn.microsoft.com/en-us/library/ms633556(v=VS.85).aspx">UpdateLayeredWindow</a>.

For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms632598(v=VS.85).aspx">Using Layered Windows</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633540(v=VS.85).aspx">SetLayeredWindowAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633591(v=VS.85).aspx">SetWindowLong</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632598(v=VS.85).aspx">Using Windows</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

