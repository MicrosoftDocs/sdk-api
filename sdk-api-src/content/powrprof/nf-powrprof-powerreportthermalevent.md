---
UID: NF:powrprof.PowerReportThermalEvent
title: PowerReportThermalEvent function (powrprof.h)
description: Notifies the operating system of thermal events.
helpviewer_keywords: ["PowerReportThermalEvent","PowerReportThermalEvent function","base.powerreportthermalevent","powrprof/PowerReportThermalEvent"]
old-location: base\powerreportthermalevent.htm
tech.root: base
ms.assetid: DD3DE1B2-17C1-4FF8-9DF8-BEF35933D913
ms.date: 12/05/2018
ms.keywords: PowerReportThermalEvent, PowerReportThermalEvent function, base.powerreportthermalevent, powrprof/PowerReportThermalEvent
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
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PowerReportThermalEvent
 - powrprof/PowerReportThermalEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - PowerReportThermalEvent
---

# PowerReportThermalEvent function


## -description

Notifies the operating system of thermal events.

## -parameters

### -param Event [in]

The thermal event structure, <a href="/windows/desktop/api/powrprof/ns-powrprof-thermal_event">THERMAL_EVENT</a>.

## -returns

Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.

## -remarks

Thermal managers call the <b>PowerReportThermalEvent</b> routine to notify the operating system of a thermal event so that the event can be recorded in the system event log.

Before calling <b>PowerReportThermalEvent</b>, the thermal manager sets the members of the <a href="/windows/desktop/api/powrprof/ns-powrprof-thermal_event">THERMAL_EVENT</a> structure to describe the thermal event.

## -see-also

<a href="/previous-versions/dn915117(v=vs.85)">Thermal management in Windows</a>