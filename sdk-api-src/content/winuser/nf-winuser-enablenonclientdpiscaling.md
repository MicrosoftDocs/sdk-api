---
UID: NF:winuser.EnableNonClientDpiScaling
title: EnableNonClientDpiScaling function
author: windows-sdk-content
description: In high-DPI displays, enables automatic display scaling of the non-client area portions of the specified top-level window. Must be called during the initialization of that window.
old-location: hidpi\enablenonclientdpiscaling.htm
old-project: hidpi
ms.assetid: 3459B040-B73F-4581-BA29-0B2F0241801E
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: EnableNonClientDpiScaling, EnableNonClientDpiScaling function [High DPI], hidpi.enablenonclientdpiscaling, winuser/EnableNonClientDpiScaling
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
-	Ext-MS-Win-NTUser-Window-l1-1-0.dll
-	Ext-MS-Win-NTUser-Window-l1-1-1.dll
-	Ext-MS-Win-NTUser-Window-l1-1-2.dll
-	ext-ms-win-ntuser-window-l1-1-3.dll
-	Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
-	EnableNonClientDpiScaling
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnableNonClientDpiScaling function


## -description


In high-DPI displays, enables automatic display scaling of the non-client area portions of the specified top-level window. Must be called during the initialization of that window.<div class="alert"><b>Note</b>  Applications running at a <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> of <b>DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2</b> automatically scale their non-client areas by default. They do not need to call this function.</div>
<div> </div>



## -parameters




### -param hwnd [in]

The window that should have automatic scaling enabled.


## -returns



If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Calling this function will enable non-client scaling for an individual top-level window with <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> of <b>DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE</b>. If instead you are not using per-window awareness, and your entire process is running in <b>DPI_AWARENESS_PER_MONITOR_AWARE</b> mode, calling this function will enable non-client scaling in top-level windows in your process.

If neither of those are true, or if you call this method from any other window, then it will fail and return a value of zero.

Non-client scaling for top-level windows is not enabled by default. You must call this API to enable it for each individual top-level window for which you wish to have the non-client area scale automatically. Once you do, there is no way to disable it. Enabling non-client scaling means that all the areas drawn by the system for the window will automatically scale in response to DPI changes on the window. That includes areas like the caption bar, the scrollbars, and the menu bar. You want to call <b>EnableNonClientDpiScaling</b> when you want the operating system to be responsible for rendering these areas automatically at the correct size based on the API of the monitor. 

Calling this function enables non-client scaling for top-level windows only. Child windows are unaffected.

This function must be called from WM_NCCREATE during the initialization of a new window. An example call might look like this:<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>case WM_NCCREATE:
{
    EnableNonClientDpiScaling(hwnd);
    return (DefWindowProc(hwnd, message, wParam, lParam));
}</pre>
</td>
</tr>
</table></span></div>




