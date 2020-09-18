---
UID: NS:powrprof._THERMAL_EVENT
title: THERMAL_EVENT (powrprof.h)
description: Contains a thermal event.
helpviewer_keywords: ["*PTHERMAL_EVENT","PTHERMAL_EVENT","PTHERMAL_EVENT structure pointer","THERMAL_EVENT","THERMAL_EVENT structure","base.thermal_event","powrprof/PTHERMAL_EVENT","powrprof/THERMAL_EVENT"]
old-location: base\thermal_event.htm
tech.root: base
ms.assetid: 80B6A494-AED6-4EF0-8B69-4AA5DA6BCBB3
ms.date: 12/05/2018
ms.keywords: '*PTHERMAL_EVENT, PTHERMAL_EVENT, PTHERMAL_EVENT structure pointer, THERMAL_EVENT, THERMAL_EVENT structure, base.thermal_event, powrprof/PTHERMAL_EVENT, powrprof/THERMAL_EVENT'
req.header: powrprof.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: THERMAL_EVENT, *PTHERMAL_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _THERMAL_EVENT
 - powrprof/_THERMAL_EVENT
 - PTHERMAL_EVENT
 - powrprof/PTHERMAL_EVENT
 - THERMAL_EVENT
 - powrprof/THERMAL_EVENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - PowrProf.h
api_name:
 - THERMAL_EVENT
---

# THERMAL_EVENT structure


## -description

Contains a thermal event.

## -struct-fields

### -field Version

The current structure version level, <b>THERMAL_EVENT_VERSION</b>.

### -field Size

The size of the structure.

### -field Type

One of the thermal event values from Ntpoapi.h: <b>THERMAL_EVENT_SHUTDOWN</b>, <b>THERMAL_EVENT_HIBERNATE</b>, or <b>THERMAL_EVENT_UNSPECIFIED</b>.

### -field Temperature

The temperature, in tenths of a degree Kelvin, that the sensor was at after crossing the trip point (or zero if unknown).

### -field TripPointTemperature

The temperature, in tenths of a degree Kelvin, of the trip point (or zero if unknown).

### -field Initiator

A pointer to a NULL-terminated, wide-character string that identifies the sensor whose threshold was crossed.

## -remarks

 Drivers use the <b>THERMAL_EVENT</b> structure to specify a thermal event. By calling the <a href="/windows/desktop/api/powrprof/nf-powrprof-powerreportthermalevent">PowerReportThermalEvent</a> routine, the operating system can record the thermal event in the system event log.

## -see-also

<a href="/previous-versions/dn915117(v=vs.85)">Thermal management in Windows</a>