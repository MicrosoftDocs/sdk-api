---
UID: NF:powersetting.PowerRegisterForEffectivePowerModeNotifications
title: PowerRegisterForEffectivePowerModeNotifications function (powersetting.h)
description: Registers a callback to receive effective power mode change notifications.
helpviewer_keywords: ["PowerRegisterForEffectivePowerModeNotifications","PowerRegisterForEffectivePowerModeNotifications function","base.powerregisterforeffectivepowermodenotifications","powersetting/PowerRegisterForEffectivePowerModeNotifications"]
old-location: base\powerregisterforeffectivepowermodenotifications.htm
tech.root: base
ms.assetid: 3C87643F-A8DA-4230-A216-8F46629BB6FB
ms.date: 12/05/2018
ms.keywords: PowerRegisterForEffectivePowerModeNotifications, PowerRegisterForEffectivePowerModeNotifications function, base.powerregisterforeffectivepowermodenotifications, powersetting/PowerRegisterForEffectivePowerModeNotifications
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
req.lib: Powrprof.lib
req.dll: Powrprof.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PowerRegisterForEffectivePowerModeNotifications
 - powersetting/PowerRegisterForEffectivePowerModeNotifications
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-power-setting-l1-1-1.dll
 - Powrprof.dll
api_name:
 - PowerRegisterForEffectivePowerModeNotifications
---

# PowerRegisterForEffectivePowerModeNotifications function


## -description

Registers a callback to receive effective power mode change notifications.

## -parameters

### -param Version

Supplies the maximum effective power mode version the caller understands. If the effective power mode comes from a later version, it is reduced to a compatible version that is then passed to the callback. 

The following values can be passed in: 
- EFFECTIVE_POWER_MODE_V1 is available starting with Windows 10, version 1809 and tracks the performance power slider and battery saver states. 
- EFFECTIVE_POWER_MODE_V2 is available starting with Windows 10, version 1903 and tracks the performance power slider, battery saver, game mode and windows mixed reality power states.

### -param Callback

A pointer to the callback to call when the effective power mode changes. This will also be called once upon registration to supply the current mode. If multiple callbacks are registered using this API, those callbacks can be called concurrently.

### -param Context

Caller-specified opaque context.

### -param RegistrationHandle

A handle to the registration. Use this handle to unregister for notifications.

## -returns

Returns S_OK (zero) if the call was successful, and a nonzero value if the call failed.

## -remarks

Immediately after registration, the callback will be invoked with the current value of the power setting. If the registration occurs while the power mode is changing, you may receive multiple callbacks; the last callback is the most recent update.

