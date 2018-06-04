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

# _CM_NOTIFY_FILTER structure


## -description


Device notification filter structure


## -struct-fields




### -field cbSize

The size of the structure.


### -field Flags

A combination of zero or more of the following flags:





#### CM_NOTIFY_FILTER_FLAG_ALL_INTERFACE_CLASSES

Register to receive notifications for PnP events for all device interface classes.  The memory at <b>pFilter-&gt;u.DeviceInterface.ClassGuid</b> must be zeroes.  Do not use this flag with CM_NOTIFY_FILTER_FLAG_ALL_DEVICE_INSTANCES.  This flag is only valid if <b>pFilter-&gt;FilterType</b> is CM_NOTIFY_FILTER_TYPE_DEVICEINTERFACE.



#### CM_NOTIFY_FILTER_FLAG_ALL_DEVICE_INSTANCES

Register to receive notifications for PnP events for all devices.  <b>pFilter-&gt;u.DeviceInstance.InstanceId</b> must be an empty string.  Do not use this flag with CM_NOTIFY_FILTER_FLAG_ALL_INTERFACE_CLASSES.  This flag is only valid if <b>pFilter-&gt;FilterType</b> is CM_NOTIFY_FILTER_TYPE_DEVICEINSTANCE.


### -field FilterType

Must be one of the following values:





#### CM_NOTIFY_FILTER_TYPE_DEVICEINTERFACE

Register for notifications for device interface events.  <b>pFilter-&gt;u.DeviceInterface.ClassGuid</b> should be filled in with the GUID of the device interface class to receive notifications for.



#### CM_NOTIFY_FILTER_TYPE_DEVICEHANDLE

Register for notifications for device handle events.  <b>pFilter-&gt;u.DeviceHandle.hTarget</b> must be filled in with a handle to the device to receive notifications for.



#### CM_NOTIFY_FILTER_TYPE_DEVICEINSTANCE

Register for notifications for device instance events. <b>pFilter-&gt;u.DeviceInstance.InstanceId</b> should be filled in with the device instance ID of the device to receive notifications for.


### -field Reserved

Set to 0.


### -field u

A union that contains information about the device to receive notifications for.


### -field u.DeviceInterface


### -field u.DeviceInterface.ClassGuid

The GUID of the device interface class for which to receive notifications.


### -field u.DeviceHandle

A handle to the device for which to receive notifications.


### -field u.DeviceHandle.hTarget

 


### -field u.DeviceInstance

The device instance ID for the device for which to receive notifications.


### -field u.DeviceInstance.InstanceId

 




## -remarks



When the driver calls the <a href="https://msdn.microsoft.com/library/windows/hardware/hh780224">CM_Register_Notification</a>
 function, it supplies a pointer to a <b>CM_NOTIFY_FILTER</b> structure in the <i>pFilter</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt299054">CM_NOTIFY_ACTION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh780224">CM_Register_Notification</a>
 

 

