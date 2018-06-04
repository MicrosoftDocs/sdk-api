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

# _STORAGE_HOTPLUG_INFO structure


## -description


Provides information about the hotplug information of a device.


## -struct-fields




### -field Size

The size of this structure, in bytes. The caller must set this member to 
      <code>sizeof(STORAGE_HOTPLUG_INFO)</code>.


### -field MediaRemovable

If this member is set to a nonzero value, the device media is removable. Otherwise, the device media is not 
      removable.


### -field MediaHotplug

If this member is set to a nonzero value, the media is not lockable. Otherwise, the device media is 
      lockable.


### -field DeviceHotplug

If this member is set to a nonzero value, the device is a hotplug device. Otherwise, the device is not a 
      hotplug device.


### -field WriteCacheEnableOverride

Reserved; set the value to <b>NULL</b>.


## -remarks



The value of the <b>Size</b> member also identifies the version of this structure, as 
    members will be added to this structure in the future. If the value of the <b>Size</b> member 
    is <code>sizeof(STORAGE_HOTPLUG_INFO)</code>, the current version of the 
    structure is the same as the version you compiled with. If the value is not 
    <code>sizeof(STORAGE_HOTPLUG_INFO)</code>, then the current version contains 
    additional members.

A hotplug device refers to a device whose <b>RemovalPolicy</b> value displayed in 
    the Device Manager is <b>ExpectSurpriseRemoval</b>. To query whether a particular device is a 
    hotplug device, use the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff560554">IOCTL_STORAGE_GET_HOTPLUG_INFO</a> operation. 
    To set the hotplug properties of a device, use the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff560606">IOCTL_STORAGE_SET_HOTPLUG_INFO</a> 
    operation.

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff560606">IOCTL_STORAGE_SET_HOTPLUG_INFO</a> 
    operation only sets the value of the <b>DeviceHotplug</b> member of this structure. If the 
    value of that member is set, the removal policy of the specified device is set to 
    <b>ExpectSurpriseRemoval</b> and all levels of caching are disabled. If the value of that 
    member is not set, the removal policy of the specified device is set 
    to <b>ExpectOrderlyRemoval</b>, and caching may be selectively enabled.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff560554">IOCTL_STORAGE_GET_HOTPLUG_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560606">IOCTL_STORAGE_SET_HOTPLUG_INFO</a>
 

 

