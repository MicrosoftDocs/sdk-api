---
UID: NF:winuser.WindowFromPhysicalPoint
title: WindowFromPhysicalPoint function
author: windows-sdk-content
description: Retrieves a handle to the window that contains the specified physical point.
old-location: winmsg\windowfromphysicalpoint.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\windowfromphysicalpoint.htm
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: WindowFromPhysicalPoint, WindowFromPhysicalPoint function [Windows and Messages], _win32_WindowFromPhysicalPoint, _win32_windowfromphysicalpoint_cpp, winmsg.windowfromphysicalpoint, winui._win32_windowfromphysicalpoint, winuser/WindowFromPhysicalPoint
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: POINTER_DEVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - minuser.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - WindowFromPhysicalPoint
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WindowFromPhysicalPoint function


## -description


Retrieves a handle to the window that contains the specified physical point.


## -parameters




### -param Point [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

The physical coordinates of the point.


## -returns



Type: <strong>Type: <b>HWND</b>
</strong>

A handle to the window that contains the given physical point. If no window exists at the point, this value is <b>NULL</b>.




## -remarks



The <b>WindowFromPhysicalPoint</b> function does not retrieve a handle to a hidden or disabled window, even if the point is within the window.




## -see-also




<a href="https://msdn.microsoft.com/library/ms632676(v=VS.85).aspx">ChildWindowFromPoint</a>



<b>Conceptual</b>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/57ecec82-03be-4d1a-84cf-6b64131af19d">WindowFromDC</a>



<a href="https://msdn.microsoft.com/library/ms633558(v=VS.85).aspx">WindowFromPoint</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt637455">Windows</a>
 

 

