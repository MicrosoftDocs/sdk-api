---
UID: NS:strmif.tagVMRMONITORINFO
title: VMRMONITORINFO (strmif.h)
description: The VMRMONITORINFO structure is used in the IVMRMonitorConfig::GetAvailableMonitors method to set and retrieve information about monitors on the system (VMR-7 only).
helpviewer_keywords: ["VMRMONITORINFO","VMRMONITORINFO structure [DirectShow]","VMRMONITORINFOStructure","dshow.vmrmonitorinfo","strmif/VMRMONITORINFO"]
old-location: dshow\vmrmonitorinfo.htm
tech.root: dshow
ms.assetid: 87567836-c01e-4615-a8e7-9ca590b6f7c9
ms.date: 12/05/2018
ms.keywords: VMRMONITORINFO, VMRMONITORINFO structure [DirectShow], VMRMONITORINFOStructure, dshow.vmrmonitorinfo, strmif/VMRMONITORINFO
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
targetos: Windows
req.typenames: VMRMONITORINFO
req.redist: 
req.product: Windows XP
ms.custom: 19H1
f1_keywords:
 - tagVMRMONITORINFO
 - strmif/tagVMRMONITORINFO
 - VMRMONITORINFO
 - strmif/VMRMONITORINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VMRMONITORINFO
---

# VMRMONITORINFO structure


## -description

The <code>VMRMONITORINFO</code> structure is used in the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrmonitorconfig-getavailablemonitors">IVMRMonitorConfig::GetAvailableMonitors</a> method to set and retrieve information about monitors on the system (VMR-7 only).

## -struct-fields

### -field guid

A [VMRGUID](/windows/desktop/api/strmif/ns-strmif-vmrguid) structure that specifies the monitor.

### -field rcMonitor

The monitor rectangle.

### -field hMon

A handle to the monitor.

### -field dwFlags

Flags as defined for the <a href="/windows/desktop/api/winuser/ns-winuser-monitorinfoexa">MONITORINFOEX</a> structure. Currently the only valid flag is <b>MONITORINFOF_PRIMARY</b>, which indicates the primary display monitor.

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

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>