---
UID: NF:winuser.PhysicalToLogicalPointForPerMonitorDPI
title: PhysicalToLogicalPointForPerMonitorDPI function (winuser.h)
description: Converts a point in a window from logical coordinates into physical coordinates, regardless of the dots per inch (dpi) awareness of the caller.
helpviewer_keywords: ["PhysicalToLogicalPointForPerMonitorDPI","PhysicalToLogicalPointForPerMonitorDPI function [High DPI]","hidpi.physicaltologicalpointforpermonitordpi","winuser/PhysicalToLogicalPointForPerMonitorDPI"]
old-location: hidpi\physicaltologicalpointforpermonitordpi.htm
tech.root: hidpi
ms.assetid: DC744BFC-4410-4878-BEA7-382550DDF9E3
ms.date: 12/05/2018
ms.keywords: PhysicalToLogicalPointForPerMonitorDPI, PhysicalToLogicalPointForPerMonitorDPI function [High DPI], hidpi.physicaltologicalpointforpermonitordpi, winuser/PhysicalToLogicalPointForPerMonitorDPI
f1_keywords:
- winuser/PhysicalToLogicalPointForPerMonitorDPI
dev_langs:
- c++
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- User32.dll
- Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
- PhysicalToLogicalPointForPerMonitorDPI
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PhysicalToLogicalPointForPerMonitorDPI function


## -description


Converts a point in a window from physical coordinates into logical coordinates, regardless of the dots per inch (dpi) awareness of the caller. For more information about DPI awareness levels, see <a href="https://docs.microsoft.com/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness">PROCESS_DPI_AWARENESS</a>.


## -parameters




### -param hWnd [in]

A handle to the window whose transform is used for the conversion.


### -param lpPoint [in, out]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a> structure that specifies the physical/screen coordinates to be converted. The new logical coordinates are copied into this structure if the function succeeds.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



In Windows 8, system–DPI aware applications translate between physical and logical space using <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-physicaltologicalpoint">PhysicalToLogicalPoint</a> and <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpoint">LogicalToPhysicalPoint</a>. In Windows 8.1, the additional virtualization of the system and inter-process communications means that for the majority of applications, you do not need these APIs. As a result, in Windows 8.1, these APIs no longer transform points. The system returns all points to an application in its own coordinate space. 
This behavior preserves functionality for the majority of applications, but there are some exceptions in which you must make changes to ensure that the application works as expected.

For example, an application might need to walk the entire window tree of another process and ask the system for DPI-dependent information about the window. By default, the system will return the information based on the DPI awareness of the caller. This is ideal for most applications. However, the caller might need the information based on the DPI awareness of the application associated with the window. This might be necessary because the two applications send DPI-dependent information between each other directly.  In this case, the application can use <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpointforpermonitordpi">LogicalToPhysicalPointForPerMonitorDPI</a> to get physical coordinates and then use <b>PhysicalToLogicalPointForPerMonitorDPI</b> to convert the physical coordinates into logical coordinates based on the DPI-awareness of the provided <b>HWND</b>.

Consider two applications, one has a <a href="https://docs.microsoft.com/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness">PROCESS_DPI_AWARENESS</a> value of <b>PROCESS_DPI_UNAWARE</b> and the other has a value of <b>PROCESS_PER_MONITOR_AWARE</b>. The  <b>PROCESS_PER_MONITOR_AWARE</b> app creates a window on a single monitor where the scale factor is 200% (192 DPI). If both apps call <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowrect">GetWindowRect</a> on this window, they will receive different values. The <b>PROCESS_DPI_UNAWARE</b> app will receive a rect based on 96 DPI coordinates, while the <b>PROCESS_PER_MONITOR_AWARE</b> app will receive coordinates matching the actual DPI of the monitor. If the <b>PROCESS_DPI_UNAWARE</b> needs the rect that the system returned to the <b>PROCESS_PER_MONITOR_AWARE</b> app, it could call <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpointforpermonitordpi">LogicalToPhysicalPointForPerMonitorDPI</a> for the corners of its rect and pass in a handle to the <b>PROCESS_PER_MONITOR_AWARE</b> app's window. This will return points based on the other app's awareness that can be used to create a rect. This works because since a <b>PROCESS_PER_MONITOR_AWARE</b> uses the actual DPI of the monitor, logical and physical coordinates are identical.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpointforpermonitordpi">LogicalToPhysicalPointForPerMonitorDPI</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness">PROCESS_DPI_AWARENESS</a>
 

 

