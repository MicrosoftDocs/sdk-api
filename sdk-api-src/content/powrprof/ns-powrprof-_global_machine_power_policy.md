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

# _GLOBAL_MACHINE_POWER_POLICY structure


## -description


Contains global computer power policy settings that apply to all power schemes for all 
   users. This structure is part of the 
   <a href="https://msdn.microsoft.com/5c177093-0c16-4a84-9212-f2376de6965b">GLOBAL_POWER_POLICY</a> structure.


## -struct-fields




### -field Revision

The current structure revision level. Set this value by calling 
      <a href="https://msdn.microsoft.com/9a834fb6-35ae-4d36-885c-0d81cd39e9a6">GetCurrentPowerPolicies</a> or 
      <a href="https://msdn.microsoft.com/65da3d9f-b688-4d41-9da0-05159297d169">ReadGlobalPwrPolicy</a> before using a 
      <b>GLOBAL_MACHINE_POWER_POLICY</b> structure 
      to set power policy.


### -field LidOpenWakeAc

The maximum power state (highest Sx value) from which a lid-open event should wake the system when running 
      on AC power. This member must be one of the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff564565">SYSTEM_POWER_STATE</a> enumeration type values. A value 
      of <b>PowerSystemUnspecified</b> indicates that a lid-open event does not wake the 
      system.


### -field LidOpenWakeDc

The maximum power state (highest Sx value) from which a lid-open event should wake the system when running 
      on battery. This member must be one of the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff564565">SYSTEM_POWER_STATE</a> enumeration type values. A value 
      of <b>PowerSystemUnspecified</b> indicates that a lid-open event does not wake the 
      system.


### -field BroadcastCapacityResolution

The resolution of change in the current battery capacity that should cause the system to be notified of a 
      system power state changed event.


## -see-also




<a href="https://msdn.microsoft.com/5c177093-0c16-4a84-9212-f2376de6965b">GLOBAL_POWER_POLICY</a>
 

 

