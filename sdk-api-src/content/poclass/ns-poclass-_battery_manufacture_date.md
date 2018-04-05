---
UID: NS:poclass._BATTERY_MANUFACTURE_DATE
title: "_BATTERY_MANUFACTURE_DATE"
author: windows-driver-content
description: Contains the date of manufacture of a battery.
old-location: base\battery_manufacture_date_str.htm
old-project: Power
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PBATTERY_MANUFACTURE_DATE, BATTERY_MANUFACTURE_DATE, BATTERY_MANUFACTURE_DATE structure, PBATTERY_MANUFACTURE_DATE, PBATTERY_MANUFACTURE_DATE structure pointer, _BATTERY_MANUFACTURE_DATE, _win32_battery_manufacture_date_str, base.battery_manufacture_date_str, batclass/BATTERY_MANUFACTURE_DATE, batclass/PBATTERY_MANUFACTURE_DATE, poclass/BATTERY_MANUFACTURE_DATE, poclass/PBATTERY_MANUFACTURE_DATE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: poclass.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Pnpxassoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BATTERY_MANUFACTURE_DATE, *PBATTERY_MANUFACTURE_DATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Poclass.h
-	Batclass.h
api_name:
-	BATTERY_MANUFACTURE_DATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _BATTERY_MANUFACTURE_DATE structure


## -description


Contains the date of manufacture of a battery. This structure is used by the 
<a href="https://msdn.microsoft.com/ef5466fe-7de8-48cd-ad48-5774d7a4bb46">BATTERY_QUERY_INFORMATION</a> structure when the BatteryManufactureDate information level is requested.


## -struct-fields




### -field Day

The day of the month of manufacture, in the range 1 to 31. In spite of the data type, this is not an ASCII encoded value. It is an unsigned byte.


### -field Month

The month of manufacture, in the range 1 (January) to 12 (December). In spite of the data type, this is not an ASCII encoded value. It is an unsigned byte.


### -field Year

The year of manufacture. This will typically be in the range 1900-2100.


## -remarks



The date is encoded in the Gregorian or western calendar format.




## -see-also




<a href="https://msdn.microsoft.com/ef5466fe-7de8-48cd-ad48-5774d7a4bb46">BATTERY_QUERY_INFORMATION</a>



<a href="https://msdn.microsoft.com/4cc89b89-ab33-47c2-8327-9627cbd1595e">IOCTL_BATTERY_QUERY_INFORMATION</a>
 

 

