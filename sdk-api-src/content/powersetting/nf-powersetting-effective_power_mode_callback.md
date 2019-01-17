---
UID: NF:powersetting.EFFECTIVE_POWER_MODE_CALLBACK
title: EFFECTIVE_POWER_MODE_CALLBACK function
author: windows-sdk-content
description: Function class for effective power mode callback.
old-location: base\effective_power_mode_callback.htm
tech.root: power
ms.assetid: 47DD6801-5120-44D3-9EE4-58CCDB4B933A
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EFFECTIVE_POWER_MODE_CALLBACK, EFFECTIVE_POWER_MODE_CALLBACK function, base.effective_power_mode_callback, powersetting/EFFECTIVE_POWER_MODE_CALLBACK
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
 - EFFECTIVE_POWER_MODE_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5
---

# EFFECTIVE_POWER_MODE_CALLBACK function


## -description


Function class for effective power mode callback.


## -parameters




### -param Mode

Indicates the effective power mode the system is running in


### -param Context

User-specified opaque context. This context would have been passed in at registration in PowerRegisterForEffectivePowerModeNotifications. 


## -returns



None.




## -remarks



Immediately after registration, this callback will be invoked with the current value of the power setting. If the registration occurs while the power setting is changing, you may receive multiple callbacks; the last callback is the most recent update. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt830297(v=VS.85).aspx">EFFECTIVE_POWER_MODE</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt830299(v=VS.85).aspx">PowerRegisterForEffectivePowerModeNotifications</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt830300(v=VS.85).aspx">PowerUnregisterFromEffectivePowerModeNotifications</a>
 

 

