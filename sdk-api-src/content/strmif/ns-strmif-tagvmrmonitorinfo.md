---
UID: NS:strmif.tagVMRMONITORINFO
title: tagVMRMONITORINFO
author: windows-sdk-content
description: The VMRMONITORINFO structure is used in the IVMRMonitorConfig::GetAvailableMonitors method to set and retrieve information about monitors on the system (VMR-7 only).
old-location: dshow\vmrmonitorinfo.htm
tech.root: DirectShow
ms.assetid: 87567836-c01e-4615-a8e7-9ca590b6f7c9
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: VMRMONITORINFO, VMRMONITORINFO structure [DirectShow], VMRMONITORINFOStructure, dshow.vmrmonitorinfo, strmif/VMRMONITORINFO, tagVMRMONITORINFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VMRMONITORINFO
product: Windows
targetos: Windows
req.typenames: VMRMONITORINFO
req.redist: 
req.product: Windows XP
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
 

 

