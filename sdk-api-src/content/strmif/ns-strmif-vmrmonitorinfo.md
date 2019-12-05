---
UID: NS:strmif.tagVMRMONITORINFO
title: VMRMONITORINFO (strmif.h)
description: The VMRMONITORINFO structure is used in the IVMRMonitorConfig::GetAvailableMonitors method to set and retrieve information about monitors on the system (VMR-7 only).
old-location: dshow\vmrmonitorinfo.htm
tech.root: DirectShow
ms.assetid: 87567836-c01e-4615-a8e7-9ca590b6f7c9
ms.date: 12/05/2018
ms.keywords: VMRMONITORINFO, VMRMONITORINFO structure [DirectShow], VMRMONITORINFOStructure, dshow.vmrmonitorinfo, strmif/VMRMONITORINFO
ms.topic: struct
f1_keywords:
- strmif/VMRMONITORINFO
dev_langs:
- c++
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
targetos: Windows
req.typenames: VMRMONITORINFO
req.redist: 
req.product: Windows XP
ms.custom: 19H1
---

# VMRMONITORINFO structure


## -description



The <code>VMRMONITORINFO</code> structure is used in the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrmonitorconfig-getavailablemonitors">IVMRMonitorConfig::GetAvailableMonitors</a> method to set and retrieve information about monitors on the system (VMR-7 only).




## -struct-fields




### -field guid

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ns-strmif-vmrguid">VMRGUID</a> structure that specifies the monitor.


### -field rcMonitor

The monitor rectangle.


### -field hMon

A handle to the monitor.
          


### -field dwFlags

Flags as defined for the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-monitorinfoexa">MONITORINFOEX</a> structure. Currently the only valid flag is <b>MONITORINFOF_PRIMARY</b>, which indicates the primary display monitor.
          


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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

