---
UID: NF:winuser.GetDpiForWindow
title: GetDpiForWindow function
author: windows-sdk-content
description: Returns the dots per inch (dpi) value for the associated window.
old-location: hidpi\getdpiforwindow.htm
old-project: hidpi
ms.assetid: E9F7BCFA-4215-44C0-95FB-57C28325720C
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: GetDpiForWindow, GetDpiForWindow function [High DPI], hidpi.getdpiforwindow, winuser/GetDpiForWindow
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetDpiForWindow
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetDpiForWindow function


## -description


Returns the dots per inch (dpi) value for the associated window.


## -parameters




### -param hwnd [in]

The window you want to get information about.


## -returns



The DPI for the window which depends on the <a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a> of the window. See the Remarks for more information. An invalid <i>hwnd</i> value will result in a return value of 0.




## -remarks



The following table indicates the return value of <b>GetDpiForWindow</b> based on the <a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a> of the provided <i>hwnd</i>.

<table>
<tr>
<th>DPI_AWARENESS</th>
<th>Return value</th>
</tr>
<tr>
<td>DPI_AWARENESS_UNAWARE</td>
<td>96</td>
</tr>
<tr>
<td>DPI_AWARENESS_SYSTEM_AWARE</td>
<td>The system DPI.</td>
</tr>
<tr>
<td>DPI_AWARENESS_PER_MONITOR_AWARE</td>
<td>The DPI of the monitor where the window is located.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a>
 

 

