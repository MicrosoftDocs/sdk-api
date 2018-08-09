---
UID: NF:winuser.GetProcessDefaultLayout
title: GetProcessDefaultLayout function
author: windows-sdk-content
description: Retrieves the default layout that is used when windows are created with no parent or owner.
old-location: winmsg\getprocessdefaultlayout.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getprocessdefaultlayout.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetProcessDefaultLayout, GetProcessDefaultLayout function [Windows and Messages], _win32_GetProcessDefaultLayout, _win32_getprocessdefaultlayout_cpp, winmsg.getprocessdefaultlayout, winui._win32_getprocessdefaultlayout, winuser/GetProcessDefaultLayout
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
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetProcessDefaultLayout
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetProcessDefaultLayout function


## -description


Retrieves the default layout that is used when windows are created with no parent or owner.


## -parameters




### -param pdwDefaultLayout [out]

Type: <b>DWORD*</b>

The current default process layout. For a list of values, see <a href="https://msdn.microsoft.com/e1a72e19-ae5e-40bf-90f2-b32078d9ac71">SetProcessDefaultLayout</a>.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The layout specifies how text and graphics are laid out in a window; the default is left to right. The <b>GetProcessDefaultLayout</b> function lets you know if the default layout has changed, from using <a href="https://msdn.microsoft.com/e1a72e19-ae5e-40bf-90f2-b32078d9ac71">SetProcessDefaultLayout</a>.




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e1a72e19-ae5e-40bf-90f2-b32078d9ac71">SetProcessDefaultLayout</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt637455">Windows</a>
 

 

