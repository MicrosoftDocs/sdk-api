---
UID: NS:batclass.BATTERY_MINIPORT_UPDATE_DATA
title: BATTERY_MINIPORT_UPDATE_DATA (batclass.h)
description: Battery miniclass drivers fill in this structure before calling the battery class driver's BatteryClassInitializeDevice routine.
helpviewer_keywords: ["*PBATTERY_MINIPORT_UPDATE_DATA","BATTERY_MINIPORT_UPDATE_DATA","BATTERY_MINIPORT_UPDATE_DATA structure [Battery Devices]","PBATTERY_MINIPORT_UPDATE_DATA","PBATTERY_MINIPORT_UPDATE_DATA structure pointer [Battery Devices]","bat-struct_0ef66c9a-61df-4c49-94f1-78e41e5b9bfb.xml","batclass/BATTERY_MINIPORT_UPDATE_DATA","batclass/PBATTERY_MINIPORT_UPDATE_DATA","battery.BATTERY_MINIPORT_UPDATE_DATA"]
old-location: battery\BATTERY_MINIPORT_UPDATE_DATA.htm
tech.root: battery
ms.assetid: db9d4e7d-a794-4c08-b849-d0b75ecf606b
ms.date: 12/05/2018
ms.keywords: '*PBATTERY_MINIPORT_UPDATE_DATA, BATTERY_MINIPORT_UPDATE_DATA, BATTERY_MINIPORT_UPDATE_DATA structure [Battery Devices], PBATTERY_MINIPORT_UPDATE_DATA, PBATTERY_MINIPORT_UPDATE_DATA structure pointer [Battery Devices], bat-struct_0ef66c9a-61df-4c49-94f1-78e41e5b9bfb.xml, batclass/BATTERY_MINIPORT_UPDATE_DATA, batclass/PBATTERY_MINIPORT_UPDATE_DATA, battery.BATTERY_MINIPORT_UPDATE_DATA'
req.header: batclass.h
req.include-header: Batclass.h
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
req.typenames: BATTERY_MINIPORT_UPDATE_DATA, *PBATTERY_MINIPORT_UPDATE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PBATTERY_MINIPORT_UPDATE_DATA
 - batclass/PBATTERY_MINIPORT_UPDATE_DATA
 - BATTERY_MINIPORT_UPDATE_DATA
 - batclass/BATTERY_MINIPORT_UPDATE_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - batclass.h
api_name:
 - BATTERY_MINIPORT_UPDATE_DATA
---

# BATTERY_MINIPORT_UPDATE_DATA structure


## -description

Battery miniclass drivers fill in this structure before calling the battery class driver's <a href="/windows/desktop/api/batclass/nf-batclass-batteryclassUpdatedata">BatteryClassUpdateData</a> routine.

## -struct-fields

### -field Version

Specifies the version number of the structure. Miniclass drivers should specify BATTERY_MINIPORT_UPDATE_DATA_VER_2.

### -field NotifyEvent

Specifies the information as specified in the <a href="/windows/desktop/api/batclass/ns-batclass-battery_non_catastrophic_event">BATTERY_NON_CATASTROPHIC_EVENT</a> struct

## -see-also

<a href="/windows/desktop/api/batclass/nf-batclass-batteryclassUpdatedata">BatteryClassUpdateData</a>.

