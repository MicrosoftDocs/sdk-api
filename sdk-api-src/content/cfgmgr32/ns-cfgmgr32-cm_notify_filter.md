---
UID: NS:cfgmgr32._CM_NOTIFY_FILTER
title: CM_NOTIFY_FILTER (cfgmgr32.h)
description: Device notification filter structure.
helpviewer_keywords: ["*PCM_NOTIFY_FILTER","CM_NOTIFY_FILTER","CM_NOTIFY_FILTER structure [Device and Driver Installation]","PCM_NOTIFY_FILTER","PCM_NOTIFY_FILTER structure pointer [Device and Driver Installation]","cfgmgr32/CM_NOTIFY_FILTER","cfgmgr32/PCM_NOTIFY_FILTER","devinst.cm_notify_filter"]
old-location: devinst\cm_notify_filter.htm
tech.root: devinst
ms.assetid: 8B6CC440-7B41-4382-9917-6833031D5E1B
ms.date: 10/06/2023
ms.keywords: '*PCM_NOTIFY_FILTER, CM_NOTIFY_FILTER, CM_NOTIFY_FILTER structure [Device and Driver Installation], PCM_NOTIFY_FILTER, PCM_NOTIFY_FILTER structure pointer [Device and Driver Installation], cfgmgr32/CM_NOTIFY_FILTER, cfgmgr32/PCM_NOTIFY_FILTER, devinst.cm_notify_filter'
req.header: cfgmgr32.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CM_NOTIFY_FILTER, *PCM_NOTIFY_FILTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CM_NOTIFY_FILTER
 - cfgmgr32/_CM_NOTIFY_FILTER
 - PCM_NOTIFY_FILTER
 - cfgmgr32/PCM_NOTIFY_FILTER
 - CM_NOTIFY_FILTER
 - cfgmgr32/CM_NOTIFY_FILTER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cfgmgr32.h
api_name:
 - CM_NOTIFY_FILTER
---

# CM_NOTIFY_FILTER structure


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

Register for notifications for device handle events.  <b>pFilter-&gt;u.DeviceHandle.hTarget</b> must be filled in with a handle to the device to receive notifications for. This handle must remain a valid handle to the device for the duration of the [CM_Register_Notification](./nf-cfgmgr32-cm_register_notification.md) call. However, after CM_Register_Notification returns, the handle can be closed without affecting the ability for the registration to receive notifications.

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

When the driver calls the <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_register_notification">CM_Register_Notification</a> function, it supplies a pointer to a <b>CM_NOTIFY_FILTER</b> structure in the <i>pFilter</i> parameter.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/ne-cfgmgr32-cm_notify_action">CM_NOTIFY_ACTION</a>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_register_notification">CM_Register_Notification</a>