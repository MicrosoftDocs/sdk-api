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

# _GLOBAL_USER_POWER_POLICY structure


## -description


Contains global user power policy settings that apply to all power schemes for a user. This structure is part of the 
<a href="https://msdn.microsoft.com/5c177093-0c16-4a84-9212-f2376de6965b">GLOBAL_POWER_POLICY</a> structure.


## -struct-fields




### -field Revision

The current structure revision level. Set this value by calling <a href="https://msdn.microsoft.com/9a834fb6-35ae-4d36-885c-0d81cd39e9a6">GetCurrentPowerPolicies</a> or  <a href="https://msdn.microsoft.com/65da3d9f-b688-4d41-9da0-05159297d169">ReadGlobalPwrPolicy</a> before using a <b>GLOBAL_USER_POWER_POLICY</b> structure to set power policy.


### -field PowerButtonAc

A 
<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a> structure that defines the action to take when the power button is pressed and the system is running on AC power.


### -field PowerButtonDc

A 
<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a> structure that defines the action to take when the power button is pressed and the system is running on battery power.


### -field SleepButtonAc

A 
<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a> structure that defines the action to take when the sleep button is pressed and the system is running on AC power.


### -field SleepButtonDc

A 
<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a> structure that defines the action to take when the sleep button is pressed and the system is running on battery power.


### -field LidCloseAc

A 
<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a> structure that defines the action to take when the lid is closed and the system is running on AC power.


### -field LidCloseDc

A 
<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a> structure that defines the action to take when the lid is closed and the system is running on battery power.


### -field DischargePolicy

An array of 
<a href="https://msdn.microsoft.com/4efa847d-92da-4cf7-95c2-c329de1691f4">SYSTEM_POWER_LEVEL</a> structures that defines the actions to take at system battery discharge events.


### -field GlobalFlags

A flag that enables or disables miscellaneous user power policy settings. This member can be one or more of the values described in 
<a href="https://msdn.microsoft.com/d98190ef-f70e-4796-960e-ff32d2cf6f4f">Global Flags Constants</a>.


## -see-also




<a href="https://msdn.microsoft.com/5c177093-0c16-4a84-9212-f2376de6965b">GLOBAL_POWER_POLICY</a>



<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a>



<a href="https://msdn.microsoft.com/4efa847d-92da-4cf7-95c2-c329de1691f4">SYSTEM_POWER_LEVEL</a>
 

 

