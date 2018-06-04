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

# tagVMRMONITORINFO structure


## -description



The <code>VMRMONITORINFO</code> structure is used in the <a href="https://msdn.microsoft.com/8a44ca7d-a195-4fcf-b09c-01f8176e0aa2">IVMRMonitorConfig::GetAvailableMonitors</a> method to set and retrieve information about monitors on the system (VMR-7 only).




## -struct-fields




### -field guid


              A <a href="https://msdn.microsoft.com/e05d986a-c044-47c9-8430-7190ad29c7ec">VMRGUID</a> structure that specifies the monitor.


### -field rcMonitor

The monitor rectangle.


### -field hMon

A handle to the monitor.
          


### -field dwFlags


            Flags as defined for the <a href="https://msdn.microsoft.com/f296ce29-3fc8-41c9-a201-56e222aa2219">MONITORINFOEX</a> structure. Currently the only valid flag is <b>MONITORINFOF_PRIMARY</b>, which indicates the primary display monitor.
          


### -field szDevice


            Null-terminated string containing the device name.
          


### -field szDescription


            Null-terminated string containing the device description.
          


### -field liDriverVersion

 


### -field dwVendorId

 


### -field dwDeviceId

 


### -field dwSubSysId

 


### -field dwRevision

 




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

