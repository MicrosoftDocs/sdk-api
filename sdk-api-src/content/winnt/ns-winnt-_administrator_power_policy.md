---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _ADMINISTRATOR_POWER_POLICY structure


## -description


Represents the administrator override power policy settings.


## -struct-fields




### -field MinSleep

The minimum system power sleep state. This member must be one of the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff564565">SYSTEM_POWER_STATE</a> enumeration type values between 
      <b>PowerSystemSleeping1</b> (power state S1) and 
      <b>PowerSystemHibernate</b> (power state S4).


### -field MaxSleep

The maximum system power sleep state. This member must be one of the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff564565">SYSTEM_POWER_STATE</a> enumeration type values between 
      <b>PowerSystemSleeping1</b> (power state S1) and 
      <b>PowerSystemHibernate</b> (power state S4).


### -field MinVideoTimeout

The minimum allowable video idle time-out before turning the display device off, in seconds.


### -field MaxVideoTimeout

The maximum allowable video idle time-out before turning the display device off, in seconds.


### -field MinSpindownTimeout

The minimum allowable disk idle time before flushing the cache manager and spinning down a hard disk 
      device, in seconds.


### -field MaxSpindownTimeout

The maximum allowable disk idle time before flushing the cache manager and spinning down a hard disk 
      device, in seconds.


## -remarks



The <b>ADMINISTRATOR_POWER_POLICY</b> 
    structure defines limits to certain power policy values that are applied globally to all users' power schemes. The 
    values in the <b>ADMINISTRATOR_POWER_POLICY</b> 
    structure override any settings selected by the user in the Power Options control panel program.

To set an administrator override policy, call the 
    <a href="https://msdn.microsoft.com/adc0052d-e2dd-4c55-996c-6af8f5987d79">CallNtPowerInformation</a> function.




## -see-also




<a href="https://msdn.microsoft.com/adc0052d-e2dd-4c55-996c-6af8f5987d79">CallNtPowerInformation</a>
 

 

