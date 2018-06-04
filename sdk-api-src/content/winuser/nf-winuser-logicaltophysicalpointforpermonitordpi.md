---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# LogicalToPhysicalPointForPerMonitorDPI function


## -description


Converts a point in a window from logical coordinates into physical coordinates, regardless of the dots per inch (dpi) awareness of the caller. For more information about DPI awareness levels, see <a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a>.


## -parameters




### -param hWnd

TBD


### -param lpPoint [in, out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that specifies the logical coordinates to be converted. The new physical coordinates are copied into this structure if the function succeeds.


#### - hwnd [in]

A handle to the window whose transform is used for the conversion.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



In Windows 8, system–DPI aware applications translated between physical and logical space using <a href="https://msdn.microsoft.com/7b02d31f-f1c7-4be1-817d-f7cc6850008d">PhysicalToLogicalPoint</a> and <a href="https://msdn.microsoft.com/a0384e46-b72f-4517-acce-a7fae7268a46">LogicalToPhysicalPoint</a>. In Windows 8.1, the additional virtualization of the system and inter-process communications means that for the majority of applications, you do not need these APIs. As a result, in Windows 8.1, these APIs no longer transform points. The system returns all points to an application in its own coordinate space. 
This behavior preserves functionality for the majority of applications, but there are some exceptions in which you must make changes to ensure that the application works as expected.

For example, an application might need to walk the entire window tree of another process and ask the system for DPI-dependent information about the window. By default, the system will return the information based on the DPI awareness of the caller. This is ideal for most applications. However, the caller might need the information based on the DPI awareness of the application associated with the window. This might be necessary because the two applications send DPI-dependent information between each other directly.  In this case, the application can use <b>LogicalToPhysicalPointForPerMonitorDPI</b> to get physical coordinates and then use <a href="https://msdn.microsoft.com/DC744BFC-4410-4878-BEA7-382550DDF9E3">PhysicalToLogicalPointForPerMonitorDPI</a> to convert the physical coordinates into logical coordinates based on the DPI-awareness of the provided <b>HWND</b>.

Consider two applications, one has a <a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a> value of <b>PROCESS_DPI_UNAWARE</b> and the other has a value of <b>PROCESS_PER_MONITOR_AWARE</b>. The  <b>PROCESS_DPI_UNAWARE</b> app creates a window on a single monitor where the scale factor is 200% (192 DPI). If both apps call <a href="https://msdn.microsoft.com/9c8fe83e-0c9a-483a-a692-4d229d1bd559">GetWindowRect</a> on this window, they will receive different values. The <b>PROCESS_DPI_UNAWARE</b> app will receive a rect based on 96 DPI coordinates, while the <b>PROCESS_PER_MONITOR_AWARE</b> app will receive coordinates matching the actual DPI of the monitor. If the <b>PROCESS_PER_MONITOR_AWARE</b> needs the rect that the system returned to the <b>PROCESS_DPI_UNAWARE</b> app, it could call <b>LogicalToPhysicalPointForPerMonitorDPI</b> for the corners of its rect and pass in the handle to the <b>PROCESS_DPI_UNAWARE</b> app's window. This will return points based on the other app's awareness that can be used to create a rect.

<div class="alert"><b>Tip</b>  <p class="note">Since an application with a <a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a> value of <b>PROCESS_PER_MONITOR_AWARE</b> uses the actual DPI of the monitor, physical and logical coordinates are the same for this app.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a>



<a href="https://msdn.microsoft.com/DC744BFC-4410-4878-BEA7-382550DDF9E3">PhysicalToLogicalPointForPerMonitorDPI</a>
 

 

