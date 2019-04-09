---
UID: NS:winnt._ADMINISTRATOR_POWER_POLICY
title: ADMINISTRATOR_POWER_POLICY (winnt.h)
author: windows-sdk-content
description: Represents the administrator override power policy settings.
old-location: base\administrator_power_policy_str.htm
tech.root: power
ms.assetid: abd2e2c5-1056-4985-ae07-a40d53bb17b1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PADMINISTRATOR_POWER_POLICY, ADMINISTRATOR_POWER_POLICY, ADMINISTRATOR_POWER_POLICY structure, PADMINISTRATOR_POWER_POLICY, PADMINISTRATOR_POWER_POLICY structure pointer, _ADMINISTRATOR_POWER_POLICY, _win32_administrator_power_policy_str, base.administrator_power_policy_str, winnt/ADMINISTRATOR_POWER_POLICY, winnt/PADMINISTRATOR_POWER_POLICY"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - ADMINISTRATOR_POWER_POLICY
product: Windows
targetos: Windows
req.typenames: ADMINISTRATOR_POWER_POLICY, *PADMINISTRATOR_POWER_POLICY
req.redist: 
---

# ADMINISTRATOR_POWER_POLICY structure


## -description


Represents the administrator override power policy settings.


## -struct-fields




### -field MinSleep

The minimum system power sleep state. This member must be one of the 
      <a href="https://msdn.microsoft.com/57436a4b-0d18-4f7e-8dc0-fc5e68b44e7d">SYSTEM_POWER_STATE</a> enumeration type values between 
      <b>PowerSystemSleeping1</b> (power state S1) and 
      <b>PowerSystemHibernate</b> (power state S4).


### -field MaxSleep

The maximum system power sleep state. This member must be one of the 
      <a href="https://msdn.microsoft.com/57436a4b-0d18-4f7e-8dc0-fc5e68b44e7d">SYSTEM_POWER_STATE</a> enumeration type values between 
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
 

 

