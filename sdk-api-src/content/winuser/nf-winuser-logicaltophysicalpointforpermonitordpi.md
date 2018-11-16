---
UID: NF:winuser.LogicalToPhysicalPointForPerMonitorDPI
title: LogicalToPhysicalPointForPerMonitorDPI function
author: windows-sdk-content
description: Converts a point in a window from logical coordinates into physical coordinates, regardless of the dots per inch (dpi) awareness of the caller.
old-location: hidpi\logicaltophysicalpointforpermonitordpi.htm
tech.root: hidpi
ms.assetid: C9ABDC73-1E96-42F1-B34D-3A649DDF02A6
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: LogicalToPhysicalPointForPerMonitorDPI, LogicalToPhysicalPointForPerMonitorDPI function [High DPI], hidpi.logicaltophysicalpointforpermonitordpi, winuser/LogicalToPhysicalPointForPerMonitorDPI
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - LogicalToPhysicalPointForPerMonitorDPI
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- LogicalToPhysicalPointForPerMonitorDPI
: 
---

# LogicalToPhysicalPointForPerMonitorDPI function


## -description


Converts a point in a window from logical coordinates into physical coordinates, regardless of the dots per inch (dpi) awareness of the caller. For more information about DPI awareness levels, see <a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a>.


## -parameters




### -param hWnd [in]

A handle to the window whose transform is used for the conversion.


### -param lpPoint [in, out]

A pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that specifies the logical coordinates to be converted. The new physical coordinates are copied into this structure if the function succeeds.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



In Windows 8, system–DPI aware applications translated between physical and logical space using <a href="https://msdn.microsoft.com/en-us/library/ms633536(v=VS.85).aspx">PhysicalToLogicalPoint</a> and <a href="https://msdn.microsoft.com/en-us/library/ms633533(v=VS.85).aspx">LogicalToPhysicalPoint</a>. In Windows 8.1, the additional virtualization of the system and inter-process communications means that for the majority of applications, you do not need these APIs. As a result, in Windows 8.1, these APIs no longer transform points. The system returns all points to an application in its own coordinate space. 
This behavior preserves functionality for the majority of applications, but there are some exceptions in which you must make changes to ensure that the application works as expected.

For example, an application might need to walk the entire window tree of another process and ask the system for DPI-dependent information about the window. By default, the system will return the information based on the DPI awareness of the caller. This is ideal for most applications. However, the caller might need the information based on the DPI awareness of the application associated with the window. This might be necessary because the two applications send DPI-dependent information between each other directly.  In this case, the application can use <b>LogicalToPhysicalPointForPerMonitorDPI</b> to get physical coordinates and then use <a href="https://msdn.microsoft.com/DC744BFC-4410-4878-BEA7-382550DDF9E3">PhysicalToLogicalPointForPerMonitorDPI</a> to convert the physical coordinates into logical coordinates based on the DPI-awareness of the provided <b>HWND</b>.

Consider two applications, one has a <a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a> value of <b>PROCESS_DPI_UNAWARE</b> and the other has a value of <b>PROCESS_PER_MONITOR_AWARE</b>. The  <b>PROCESS_DPI_UNAWARE</b> app creates a window on a single monitor where the scale factor is 200% (192 DPI). If both apps call <a href="https://msdn.microsoft.com/en-us/library/ms633519(v=VS.85).aspx">GetWindowRect</a> on this window, they will receive different values. The <b>PROCESS_DPI_UNAWARE</b> app will receive a rect based on 96 DPI coordinates, while the <b>PROCESS_PER_MONITOR_AWARE</b> app will receive coordinates matching the actual DPI of the monitor. If the <b>PROCESS_PER_MONITOR_AWARE</b> needs the rect that the system returned to the <b>PROCESS_DPI_UNAWARE</b> app, it could call <b>LogicalToPhysicalPointForPerMonitorDPI</b> for the corners of its rect and pass in the handle to the <b>PROCESS_DPI_UNAWARE</b> app's window. This will return points based on the other app's awareness that can be used to create a rect.

<div class="alert"><b>Tip</b>  <p class="note">Since an application with a <a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a> value of <b>PROCESS_PER_MONITOR_AWARE</b> uses the actual DPI of the monitor, physical and logical coordinates are the same for this app.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a>



<a href="https://msdn.microsoft.com/DC744BFC-4410-4878-BEA7-382550DDF9E3">PhysicalToLogicalPointForPerMonitorDPI</a>
 

 

