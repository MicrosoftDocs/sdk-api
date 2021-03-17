---
UID: NS:winioctl._STORAGE_HOTPLUG_INFO
title: STORAGE_HOTPLUG_INFO
description: Provides information about the hotplug information of a device.
helpviewer_keywords: ["*PSTORAGE_HOTPLUG_INFO","PSTORAGE_HOTPLUG_INFO","PSTORAGE_HOTPLUG_INFO structure pointer","STORAGE_HOTPLUG_INFO","STORAGE_HOTPLUG_INFO structure","_win32_storage_hotplug_info_str","base.storage_hotplug_info_str","winioctl/PSTORAGE_HOTPLUG_INFO","winioctl/STORAGE_HOTPLUG_INFO"]
old-location: base\storage_hotplug_info_str.htm
tech.root: base
ms.assetid: 861e6067-9f37-427a-8d3b-8cb9d0f95c40
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_HOTPLUG_INFO, PSTORAGE_HOTPLUG_INFO, PSTORAGE_HOTPLUG_INFO structure pointer, STORAGE_HOTPLUG_INFO, STORAGE_HOTPLUG_INFO structure, _win32_storage_hotplug_info_str, base.storage_hotplug_info_str, winioctl/PSTORAGE_HOTPLUG_INFO, winioctl/STORAGE_HOTPLUG_INFO'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.typenames: STORAGE_HOTPLUG_INFO, *PSTORAGE_HOTPLUG_INFO
req.redist: 
f1_keywords:
 - _STORAGE_HOTPLUG_INFO
 - winioctl/_STORAGE_HOTPLUG_INFO
 - PSTORAGE_HOTPLUG_INFO
 - winioctl/PSTORAGE_HOTPLUG_INFO
 - STORAGE_HOTPLUG_INFO
 - winioctl/STORAGE_HOTPLUG_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - STORAGE_HOTPLUG_INFO
---

# STORAGE_HOTPLUG_INFO structure


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
    <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_hotplug_info">IOCTL_STORAGE_GET_HOTPLUG_INFO</a> operation. 
    To set the hotplug properties of a device, use the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_set_hotplug_info">IOCTL_STORAGE_SET_HOTPLUG_INFO</a> 
    operation.

The <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_set_hotplug_info">IOCTL_STORAGE_SET_HOTPLUG_INFO</a> 
    operation only sets the value of the <b>DeviceHotplug</b> member of this structure. If the 
    value of that member is set, the removal policy of the specified device is set to 
    <b>ExpectSurpriseRemoval</b> and all levels of caching are disabled. If the value of that 
    member is not set, the removal policy of the specified device is set 
    to <b>ExpectOrderlyRemoval</b>, and caching may be selectively enabled.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_hotplug_info">IOCTL_STORAGE_GET_HOTPLUG_INFO</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_set_hotplug_info">IOCTL_STORAGE_SET_HOTPLUG_INFO</a>