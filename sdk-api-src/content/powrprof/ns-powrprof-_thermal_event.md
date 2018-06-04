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

# _THERMAL_EVENT structure


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



 Drivers use the <b>THERMAL_EVENT</b> structure to specify a thermal event. By calling the <a href="https://msdn.microsoft.com/DD3DE1B2-17C1-4FF8-9DF8-BEF35933D913">PowerReportThermalEvent</a> routine, the operating system can record the thermal event in the system event log.




## -see-also




<a href="https://msdn.microsoft.com/39B0258F-FD2E-4507-847B-8469881C126C">Thermal management in Windows</a>
 

 

