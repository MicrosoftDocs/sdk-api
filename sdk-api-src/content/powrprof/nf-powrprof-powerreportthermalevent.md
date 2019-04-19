---
UID: NF:powrprof.PowerReportThermalEvent
title: PowerReportThermalEvent function (powrprof.h)
author: windows-sdk-content
description: Notifies the operating system of thermal events.
old-location: base\powerreportthermalevent.htm
tech.root: power
ms.assetid: DD3DE1B2-17C1-4FF8-9DF8-BEF35933D913
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PowerReportThermalEvent, PowerReportThermalEvent function, base.powerreportthermalevent, powrprof/PowerReportThermalEvent
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - PowerReportThermalEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PowerReportThermalEvent function


## -description


Notifies the operating system of thermal events.


## -parameters




### -param Event [in]

The thermal event structure, <a href="https://msdn.microsoft.com/80B6A494-AED6-4EF0-8B69-4AA5DA6BCBB3">THERMAL_EVENT</a>.


## -returns



Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.




## -remarks



Thermal managers call the <b>PowerReportThermalEvent</b> routine to notifiy the operating system of a thermal event so that the event can be recorded in the system event log.

Before calling <b>PowerReportThermalEvent</b>, the thermal manager sets the members of the <a href="https://msdn.microsoft.com/80B6A494-AED6-4EF0-8B69-4AA5DA6BCBB3">THERMAL_EVENT</a> structure to describe the thermal event.




## -see-also




<a href="https://msdn.microsoft.com/39B0258F-FD2E-4507-847B-8469881C126C">Thermal management in Windows</a>
 

 

