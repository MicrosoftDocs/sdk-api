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

# _VMR9MonitorInfo structure


## -description



The <code>VMR9MonitorInfo</code> structure is used with the VMR-9 in the <a href="https://msdn.microsoft.com/cebd40c2-ea41-4ed1-87d1-37f9d427c539">IVMRMonitorConfig9::GetAvailableMonitors</a> method to set and retrieve information about monitors on the system.




## -struct-fields




### -field uDevID

Integer index that specifies the monitor device.


### -field rcMonitor

Specifies the monitor's rectangle.


### -field hMon

Handle to the monitor.


### -field dwFlags


            
            Flags as defined for the <a href="https://msdn.microsoft.com/f296ce29-3fc8-41c9-a201-56e222aa2219">MONITORINFOEX</a> structure. Currently the only valid flag is <b>MONITORINFOF_PRIMARY</b>, which indicates the primary display monitor.
          


### -field szDevice

Null-terminated string containing the device name.


### -field szDescription

Null-terminated string containing a description of the device.


### -field liDriverVersion

Specifies the driver version.


### -field dwVendorId

Specifies the vendor.


### -field dwDeviceId

Specifies the device ID.


### -field dwSubSysId

Specifies the device subsystem.


### -field dwRevision

Specifies the revision number.


## -remarks



This structure is used to configure monitors on multi-monitor systems.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

