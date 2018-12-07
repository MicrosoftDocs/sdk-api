---
UID: NF:powersetting.PowerUnregisterFromEffectivePowerModeNotifications
title: PowerUnregisterFromEffectivePowerModeNotifications function
author: windows-sdk-content
description: Unregisters from effective power mode change notifications. This function is intended to be called from cleanup code and will wait for all callbacks to complete before unregistering.
old-location: base\powerunregisterfromeffectivepowermodenotifications.htm
tech.root: power
ms.assetid: 6E9AB09B-B082-406C-8F2D-43BEA04C19E0
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: PowerUnregisterFromEffectivePowerModeNotifications, PowerUnregisterFromEffectivePowerModeNotifications function, base.powerunregisterfromeffectivepowermodenotifications, powersetting/PowerUnregisterFromEffectivePowerModeNotifications
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Powrprof.dll
api_name:
 - PowerUnregisterFromEffectivePowerModeNotifications
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PowerUnregisterFromEffectivePowerModeNotifications function


## -description


Unregisters from effective power mode change notifications. This function is intended to be called from cleanup code and will wait for all callbacks to complete before unregistering. 


## -parameters




### -param RegistrationHandle

The handle corresponding to a single power mode registration. This handle should have been saved by the caller after the call to <a href="base.powerregisterforeffectivepowermodenotifications">PowerRegisterForEffectivePowerModeNotifications</a> and passed in here. 


## -returns



Returns S_OK (zero) if the call was successful, and a nonzero value if the call failed.




## -remarks



Immediately after registration, the callback will be invoked with the current value of the power setting. If the registration occurs while the power setting is changing, you may receive multiple callbacks; the last callback is the most recent update.




## -see-also




<a href="base.powerregisterforeffectivepowermodenotifications">PowerRegisterForEffectivePowerModeNotifications</a>
 

 

