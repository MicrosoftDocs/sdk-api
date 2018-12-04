---
UID: NF:winuser.GetNextWindow
title: GetNextWindow macro
author: windows-sdk-content
description: Retrieves a handle to the next or previous window in the Z-Order. The next window is below the specified window; the previous window is above.
old-location: winmsg\getnextwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getnextwindow.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GW_HWNDNEXT, GW_HWNDPREV, GetNextWindow, GetNextWindow function [Windows and Messages], _win32_GetNextWindow, _win32_getnextwindow_cpp, winmsg.getnextwindow, winui._win32_getnextwindow, winuser/GetNextWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - GetNextWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNextWindow macro


## -description


Retrieves a handle to the next or previous window in the <a href="window_features.htm">Z-Order</a>. The next window is below the specified window; the previous window is above.

If the specified window is a topmost window, the function searches for a topmost window. If the specified window is a top-level window, the function searches for a top-level window. If the specified window is a child window, the function searches for a child window.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to a window. The window handle retrieved is relative to this window, based on the value of the <i>wCmd</i> parameter. 


### -param wCmd [in]

Type: <b>UINT</b>

Indicates whether the function returns a handle to the next window or the previous window. This parameter can be either of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GW_HWNDNEXT"></a><a id="gw_hwndnext"></a><dl>
<dt><b>GW_HWNDNEXT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Returns a handle to the window below the given window.

</td>
</tr>
<tr>
<td width="40%"><a id="GW_HWNDPREV"></a><a id="gw_hwndprev"></a><dl>
<dt><b>GW_HWNDPREV</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Returns a handle to the window above the given window.

</td>
</tr>
</table>
 


## -remarks



This function is implemented as a call to the <a href="https://msdn.microsoft.com/837f8d99-abc5-4c7c-a363-3d178e71aea2">GetWindow</a> function.

<pre class="syntax" xml:space="preserve"><code>#define GetNextWindow(hWnd, wCmd) GetWindow(hWnd, wCmd)</code></pre>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/743eb915-5283-4000-954c-d68fa384ab5c">GetTopWindow</a>



<a href="https://msdn.microsoft.com/837f8d99-abc5-4c7c-a363-3d178e71aea2">GetWindow</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

