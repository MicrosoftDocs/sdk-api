---
UID: NF:winuser.CascadeWindows
title: CascadeWindows function
author: windows-sdk-content
description: Cascades the specified child windows of the specified parent window.
old-location: winmsg\cascadewindows.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\cascadewindows.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CascadeWindows, CascadeWindows function [Windows and Messages], MDITILE_SKIPDISABLED, MDITILE_ZORDER, _win32_CascadeWindows, _win32_cascadewindows_cpp, winmsg.cascadewindows, winui._win32_cascadewindows, winuser/CascadeWindows
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - CascadeWindows
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CascadeWindows function


## -description


Cascades the specified child windows of the specified parent window.


## -parameters




### -param hwndParent [in, optional]

Type: <b>HWND</b>

A handle to the parent window. If this parameter is <b>NULL</b>, the desktop window is assumed. 


### -param wHow [in]

Type: <b>UINT</b>

A cascade flag. This parameter can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MDITILE_SKIPDISABLED"></a><a id="mditile_skipdisabled"></a><dl>
<dt><b>MDITILE_SKIPDISABLED</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Prevents disabled MDI child windows from being cascaded. 

</td>
</tr>
<tr>
<td width="40%"><a id="MDITILE_ZORDER"></a><a id="mditile_zorder"></a><dl>
<dt><b>MDITILE_ZORDER</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Arranges the windows in Z order. If this value is not specified, the windows are arranged using the order specified in the <i>lpKids</i> array. 

</td>
</tr>
</table>
 


### -param lpRect [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a structure that specifies the rectangular area, in client coordinates, within which the windows are arranged. This parameter can be <b>NULL</b>, in which case the client area of the parent window is used. 


### -param cKids [in]

Type: <b>UINT</b>

The number of elements in the array specified by the 
<i>lpKids</i> parameter. This parameter is ignored if <i>lpKids</i> is <b>NULL</b>. 


### -param lpKids [in, optional]

Type: <b>const HWND*</b>

An array of handles to the child windows to arrange. If a specified child window is a top-level window with the style <b>WS_EX_TOPMOST</b> or <b>WS_EX_TOOLWINDOW</b>, the child window is not arranged. If this parameter is <b>NULL</b>, all child windows of the specified parent window (or of the desktop window) are arranged. 


## -returns



Type: <strong>Type: <b>WORD</b>
</strong>

If the function succeeds, the return value is the number of windows arranged.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



By default, <b>CascadeWindows</b> arranges the windows in the order provided by the <i>lpKids</i> array, but preserves the <a href="https://msdn.microsoft.com/en-us/library/ms632599(v=VS.85).aspx">Z-Order</a>. If you specify the <b>MDITILE_ZORDER</b> flag, <b>CascadeWindows</b> arranges the windows in Z order. 

Calling <b>CascadeWindows</b> causes all maximized windows to be restored to their previous size. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows Overview</a>
 

 

