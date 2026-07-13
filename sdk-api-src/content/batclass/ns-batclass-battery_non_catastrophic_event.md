---
UID: NS:batclass.BATTERY_NON_CATASTROPHIC_EVENT
title: BATTERY_NON_CATASTROPHIC_EVENT (batclass.h)
description: A battery miniclass driver receives a BATTERY_NON_CATASTROPHIC_EVENT structure when its BatteryMiniSetStatusNotify routine is called.
helpviewer_keywords: ["*PBATTERY_NON_CATASTROPHIC_EVENT","BATTERY_NON_CATASTROPHIC_EVENT","BATTERY_NON_CATASTROPHIC_EVENT structure [Battery Devices]","PBATTERY_NON_CATASTROPHIC_EVENT","PBATTERY_NON_CATASTROPHIC_EVENT structure pointer [Battery Devices]","bat-struct_cd1e6dc5-678c-4529-b852-2832ce2e791b.xml","batclass/BATTERY_NON_CATASTROPHIC_EVENT","batclass/PBATTERY_NON_CATASTROPHIC_EVENT","battery.BATTERY_NON_CATASTROPHIC_EVENT"]
old-location: battery\BATTERY_NON_CATASTROPHIC_EVENT.htm
tech.root: battery
ms.assetid: 5bf89418-1d18-460b-b1d1-db6fbb390bc8
ms.date: 12/05/2018
ms.keywords: '*PBATTERY_NON_CATASTROPHIC_EVENT, BATTERY_NON_CATASTROPHIC_EVENT, BATTERY_NON_CATASTROPHIC_EVENT structure [Battery Devices], PBATTERY_NON_CATASTROPHIC_EVENT, PBATTERY_NON_CATASTROPHIC_EVENT structure pointer [Battery Devices], bat-struct_cd1e6dc5-678c-4529-b852-2832ce2e791b.xml, batclass/BATTERY_NON_CATASTROPHIC_EVENT, batclass/PBATTERY_NON_CATASTROPHIC_EVENT, battery.BATTERY_NON_CATASTROPHIC_EVENT'
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
req.typenames: BATTERY_NON_CATASTROPHIC_EVENT, *PBATTERY_NON_CATASTROPHIC_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PBATTERY_NON_CATASTROPHIC_EVENT
 - batclass/PBATTERY_NON_CATASTROPHIC_EVENT
 - BATTERY_NON_CATASTROPHIC_EVENT
 - batclass/BATTERY_NON_CATASTROPHIC_EVENT
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
 - BATTERY_NON_CATASTROPHIC_EVENT
---

# BATTERY_NON_CATASTROPHIC_EVENT structure


## -description

A battery miniclass driver fill BATTERY_NON_CATASTROPHIC_EVENT structure when it notify class driver about battery data update <a href="/windows/desktop/api/batclass/nf-batclass-batteryclassUpdatedata">BatteryClassUpdateData</a>.

## -struct-fields

### -field BatteryChargeLimitState

This is one bit, when set miniport notifying the class driver that battery is charge limit state, flase otherwise.

### -field BatteryChargingState

This is 2 bit, miniport specify one of the enum value BatteryNoPowerSupply, BatteryInadequatePowerSupply or BatteryAdequatePowerSupply

### -field Reserved

Rest 29 bits are reserved and not-used..

## -see-also

<a href="/windows/desktop/api/batclass/nf-batclass-batteryclassUpdatedata">BatteryClassUpdateData</a>.

