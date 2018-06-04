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
 

 

