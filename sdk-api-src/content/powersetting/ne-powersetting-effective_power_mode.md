---
UID: NE:powersetting.EFFECTIVE_POWER_MODE
title: EFFECTIVE_POWER_MODE (powersetting.h)
description: Indicates the effective power mode the system is running.
helpviewer_keywords: ["EFFECTIVE_POWER_MODE","EFFECTIVE_POWER_MODE enumeration","EffectivePowerModeBalanced","EffectivePowerModeBatterySaver","EffectivePowerModeBetterBattery","EffectivePowerModeHighPerformance","EffectivePowerModeInvalid","EffectivePowerModeMaxPerformance","base.effective_power_mode","powersetting/EFFECTIVE_POWER_MODE","powersetting/EffectivePowerModeBalanced","powersetting/EffectivePowerModeBatterySaver","powersetting/EffectivePowerModeBetterBattery","powersetting/EffectivePowerModeHighPerformance","powersetting/EffectivePowerModeInvalid","powersetting/EffectivePowerModeMaxPerformance"]
old-location: base\effective_power_mode.htm
tech.root: base
ms.assetid: 8FA09CC0-99E7-4B05-88A0-2AF406C7B60C
ms.date: 12/05/2018
ms.keywords: EFFECTIVE_POWER_MODE, EFFECTIVE_POWER_MODE enumeration, EffectivePowerModeBalanced, EffectivePowerModeBatterySaver, EffectivePowerModeBetterBattery, EffectivePowerModeHighPerformance, EffectivePowerModeInvalid, EffectivePowerModeMaxPerformance, base.effective_power_mode, powersetting/EFFECTIVE_POWER_MODE, powersetting/EffectivePowerModeBalanced, powersetting/EffectivePowerModeBatterySaver, powersetting/EffectivePowerModeBetterBattery, powersetting/EffectivePowerModeHighPerformance, powersetting/EffectivePowerModeInvalid, powersetting/EffectivePowerModeMaxPerformance
f1_keywords:
- powersetting/EFFECTIVE_POWER_MODE
dev_langs:
- c++
req.header: powersetting.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: None supported
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
- Powersetting.h
api_name:
- EFFECTIVE_POWER_MODE
targetos: Windows
req.typenames: EFFECTIVE_POWER_MODE
req.redist: 
ms.custom: RS5, 19H1
---

# EFFECTIVE_POWER_MODE enumeration


## -description


Indicates the effective power mode the system is running.


## -enum-fields




### -field EffectivePowerModeBatterySaver

The system is in battery saver mode.


### -field EffectivePowerModeBetterBattery

The system is in the better battery effective power mode. 

<div class="alert"><b>Note</b>  For systems using the legacy high performance overlay, this effective power mode will never be used.</div>
<div> </div>

### -field EffectivePowerModeBalanced

The system is in the balanced effective power mode.


### -field EffectivePowerModeHighPerformance

The system is in the high performance effective power mode. 

<div class="alert"><b>Note</b>  This effective power mode is only used for systems using the legacy high performance overlay.</div>
<div> </div>

### -field EffectivePowerModeMaxPerformance

The system is in the maximum performance effective power mode.


### -field EffectivePowerModeGameMode

The system is in game mode power mode. 

<div class="alert"><b>Note</b> This mode is only available with the EFFECTIVE_POWER_MODE_V2 version of the API </div>
<div> </div>

### -field EffectivePowerModeMixedReality

The system is in the windows mixed reality power mode. 

<div class="alert"><b>Note</b> This mode is only available with the EFFECTIVE_POWER_MODE_V2 version of the API </div>
<div> </div>
