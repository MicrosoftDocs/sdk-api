---
UID: NS:winnt.SYSTEM_BATTERY_STATE
title: SYSTEM_BATTERY_STATE (winnt.h)
description: Contains information about the current state of the system battery.
helpviewer_keywords: ["*PSYSTEM_BATTERY_STATE","PSYSTEM_BATTERY_STATE","PSYSTEM_BATTERY_STATE structure pointer","SYSTEM_BATTERY_STATE","SYSTEM_BATTERY_STATE structure","_win32_system_battery_state_str","base.system_battery_state_str","winnt/PSYSTEM_BATTERY_STATE","winnt/SYSTEM_BATTERY_STATE"]
old-location: base\system_battery_state_str.htm
tech.root: base
ms.assetid: 6eed7c93-48bd-4142-b639-df6d71b114f9
ms.date: 12/05/2018
ms.keywords: '*PSYSTEM_BATTERY_STATE, PSYSTEM_BATTERY_STATE, PSYSTEM_BATTERY_STATE structure pointer, SYSTEM_BATTERY_STATE, SYSTEM_BATTERY_STATE structure, _win32_system_battery_state_str, base.system_battery_state_str, winnt/PSYSTEM_BATTERY_STATE, winnt/SYSTEM_BATTERY_STATE'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: SYSTEM_BATTERY_STATE, *PSYSTEM_BATTERY_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSYSTEM_BATTERY_STATE
 - winnt/PSYSTEM_BATTERY_STATE
 - SYSTEM_BATTERY_STATE
 - winnt/SYSTEM_BATTERY_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - SYSTEM_BATTERY_STATE
---

# SYSTEM_BATTERY_STATE structure


## -description

Contains information about the current state of the system battery.

## -struct-fields

### -field AcOnLine

If this member is <b>TRUE</b>, the system battery charger is currently operating on external 
      power.

### -field BatteryPresent

If this member is <b>TRUE</b>, at least one battery is present in the system.

### -field Charging

If this member is <b>TRUE</b>, a battery is currently charging.

### -field Discharging

If this member is <b>TRUE</b>, a battery is currently discharging.

### -field Spare1

Reserved.

### -field Tag

### -field MaxCapacity

The theoretical capacity of the battery when new.

### -field RemainingCapacity

The estimated remaining capacity of the battery.

### -field Rate

The current rate of discharge of the battery, in mW. A nonzero, positive rate indicates charging; a 
      negative rate indicates discharging. Some batteries report only discharging rates. This value should be treated 
      as a <b>LONG</b> as it can contain negative values (with the high bit set).

### -field EstimatedTime

The estimated time remaining on the battery, in seconds.

### -field DefaultAlert1

The manufacturer's suggestion of a capacity, in mWh, at which a low battery alert should occur. Definitions 
      of low vary from manufacturer to manufacturer. In general, a warning state will occur before a low state, but 
      you should not assume that it always will. To reduce risk of data loss, this value is usually used as the 
      default setting for the critical battery alarm.

### -field DefaultAlert2

The manufacturer's suggestion of a capacity, in mWh, at which a warning battery alert should occur. 
      Definitions of warning vary from manufacturer to manufacturer. In general, a warning state will occur before a 
      low state, but you should not assume that it always will. To reduce risk of data loss, this value is usually 
      used as the default setting for the low battery alarm.

## -see-also

<a href="/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a>

