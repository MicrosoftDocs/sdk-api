---
UID: NS:winnt._HARDWARE_COUNTER_DATA
title: "_HARDWARE_COUNTER_DATA"
author: windows-sdk-content
description: Contains the hardware counter value.
old-location: hcp\hardware_counter_data.htm
tech.root: hcp
ms.assetid: 7224b623-c097-44e8-b9da-5fdfad3fb505
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: "*PHARDWARE_COUNTER_DATA, HARDWARE_COUNTER_DATA, HARDWARE_COUNTER_DATA structure [Hardware Counter Profiling], PHARDWARE_COUNTER_DATA, PHARDWARE_COUNTER_DATA structure pointer [Hardware Counter Profiling], _HARDWARE_COUNTER_DATA, hcp.hardware_counter_data, winnt/HARDWARE_COUNTER_DATA, winnt/PHARDWARE_COUNTER_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Winnt.h
api_name:
 - HARDWARE_COUNTER_DATA
product: Windows
targetos: Windows
req.typenames: HARDWARE_COUNTER_DATA, *PHARDWARE_COUNTER_DATA
req.redist: 
---

# _HARDWARE_COUNTER_DATA structure


## -description


Contains the hardware counter value.


## -struct-fields




### -field Type

The type of hardware counter data collected. For possible values, see the <a href="https://msdn.microsoft.com/250dd9f1-b409-4b17-bb84-bf7eba14d36e">HARDWARE_COUNTER_TYPE</a> enumeration.


### -field Reserved

Reserved. Initialize to zero.


### -field Value

The counter index. Each hardware counter in a processor's performance monitoring unit (PMU) is identified by an index.


## -remarks



This structure is a member of the <a href="https://msdn.microsoft.com/468060cc-7b17-4ef4-8ae0-74d2bfcd5e4a">PERFORMANCE_DATA</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/468060cc-7b17-4ef4-8ae0-74d2bfcd5e4a">PERFORMANCE_DATA</a>
 

 

