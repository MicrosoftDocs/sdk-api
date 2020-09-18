---
UID: NS:winnt._HARDWARE_COUNTER_DATA
title: HARDWARE_COUNTER_DATA (winnt.h)
description: Contains the hardware counter value.
helpviewer_keywords: ["*PHARDWARE_COUNTER_DATA","HARDWARE_COUNTER_DATA","HARDWARE_COUNTER_DATA structure [Hardware Counter Profiling]","PHARDWARE_COUNTER_DATA","PHARDWARE_COUNTER_DATA structure pointer [Hardware Counter Profiling]","_HARDWARE_COUNTER_DATA","hcp.hardware_counter_data","winnt/HARDWARE_COUNTER_DATA","winnt/PHARDWARE_COUNTER_DATA"]
old-location: hcp\hardware_counter_data.htm
tech.root: hcp
ms.assetid: 7224b623-c097-44e8-b9da-5fdfad3fb505
ms.date: 12/05/2018
ms.keywords: '*PHARDWARE_COUNTER_DATA, HARDWARE_COUNTER_DATA, HARDWARE_COUNTER_DATA structure [Hardware Counter Profiling], PHARDWARE_COUNTER_DATA, PHARDWARE_COUNTER_DATA structure pointer [Hardware Counter Profiling], _HARDWARE_COUNTER_DATA, hcp.hardware_counter_data, winnt/HARDWARE_COUNTER_DATA, winnt/PHARDWARE_COUNTER_DATA'
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
targetos: Windows
req.typenames: HARDWARE_COUNTER_DATA, *PHARDWARE_COUNTER_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HARDWARE_COUNTER_DATA
 - winnt/_HARDWARE_COUNTER_DATA
 - PHARDWARE_COUNTER_DATA
 - winnt/PHARDWARE_COUNTER_DATA
 - HARDWARE_COUNTER_DATA
 - winnt/HARDWARE_COUNTER_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - HARDWARE_COUNTER_DATA
---

# HARDWARE_COUNTER_DATA structure


## -description

Contains the hardware counter value.

## -struct-fields

### -field Type

The type of hardware counter data collected. For possible values, see the <a href="/windows/desktop/api/winnt/ne-winnt-hardware_counter_type">HARDWARE_COUNTER_TYPE</a> enumeration.

### -field Reserved

Reserved. Initialize to zero.

### -field Value

The counter index. Each hardware counter in a processor's performance monitoring unit (PMU) is identified by an index.

## -remarks

This structure is a member of the <a href="/windows/desktop/api/winnt/ns-winnt-performance_data">PERFORMANCE_DATA</a> structure.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-performance_data">PERFORMANCE_DATA</a>