---
UID: NF:powersetting.PowerUnregisterFromEffectivePowerModeNotifications
title: PowerUnregisterFromEffectivePowerModeNotifications function (powersetting.h)
description: Unregisters from effective power mode change notifications. This function is intended to be called from cleanup code and will wait for all callbacks to complete before unregistering.
helpviewer_keywords: ["PowerUnregisterFromEffectivePowerModeNotifications","PowerUnregisterFromEffectivePowerModeNotifications function","base.powerunregisterfromeffectivepowermodenotifications","powersetting/PowerUnregisterFromEffectivePowerModeNotifications"]
old-location: base\powerunregisterfromeffectivepowermodenotifications.htm
tech.root: base
ms.assetid: 6E9AB09B-B082-406C-8F2D-43BEA04C19E0
ms.date: 12/05/2018
ms.keywords: PowerUnregisterFromEffectivePowerModeNotifications, PowerUnregisterFromEffectivePowerModeNotifications function, base.powerunregisterfromeffectivepowermodenotifications, powersetting/PowerUnregisterFromEffectivePowerModeNotifications
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
 - PowerUnregisterFromEffectivePowerModeNotifications
 - powersetting/PowerUnregisterFromEffectivePowerModeNotifications
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
 - PowerUnregisterFromEffectivePowerModeNotifications
---

# PowerUnregisterFromEffectivePowerModeNotifications function


## -description

Unregisters from effective power mode change notifications. This function is intended to be called from cleanup code and will wait for all callbacks to complete before unregistering.

## -parameters

### -param RegistrationHandle

The handle corresponding to a single power mode registration. This handle should have been saved by the caller after the call to <a href="../powersetting/nf-powersetting-powerregisterforeffectivepowermodenotifications.md">PowerRegisterForEffectivePowerModeNotifications</a> and passed in here.

## -returns

Returns S_OK (zero) if the call was successful, and a nonzero value if the call failed.

## -remarks

Immediately after registration, the callback will be invoked with the current value of the power setting. If the registration occurs while the power setting is changing, you may receive multiple callbacks; the last callback is the most recent update.

## -see-also

<a href="../powersetting/nf-powersetting-powerregisterforeffectivepowermodenotifications.md">PowerRegisterForEffectivePowerModeNotifications</a>

