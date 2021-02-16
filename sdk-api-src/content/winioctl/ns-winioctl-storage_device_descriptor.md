---
UID: NS:winioctl._STORAGE_DEVICE_DESCRIPTOR
title: STORAGE_DEVICE_DESCRIPTOR
description: Used in conjunction with the IOCTL_STORAGE_QUERY_PROPERTY control code to retrieve the storage device descriptor data for a device.
helpviewer_keywords: ["*PSTORAGE_DEVICE_DESCRIPTOR","PSTORAGE_DEVICE_DESCRIPTOR","PSTORAGE_DEVICE_DESCRIPTOR structure pointer [Files]","STORAGE_DEVICE_DESCRIPTOR","STORAGE_DEVICE_DESCRIPTOR structure [Files]","fs.storage_device_descriptor","winioctl/PSTORAGE_DEVICE_DESCRIPTOR","winioctl/STORAGE_DEVICE_DESCRIPTOR"]
old-location: fs\storage_device_descriptor.htm
tech.root: fs
ms.assetid: f84f8a88-b6fc-4b22-b858-52955c8d537d
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_DEVICE_DESCRIPTOR, PSTORAGE_DEVICE_DESCRIPTOR, PSTORAGE_DEVICE_DESCRIPTOR structure pointer [Files], STORAGE_DEVICE_DESCRIPTOR, STORAGE_DEVICE_DESCRIPTOR structure [Files], fs.storage_device_descriptor, winioctl/PSTORAGE_DEVICE_DESCRIPTOR, winioctl/STORAGE_DEVICE_DESCRIPTOR'
req.header: winioctl.h
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
targetos: Windows
req.typenames: STORAGE_DEVICE_DESCRIPTOR, *PSTORAGE_DEVICE_DESCRIPTOR
req.redist: 
f1_keywords:
 - _STORAGE_DEVICE_DESCRIPTOR
 - winioctl/_STORAGE_DEVICE_DESCRIPTOR
 - PSTORAGE_DEVICE_DESCRIPTOR
 - winioctl/PSTORAGE_DEVICE_DESCRIPTOR
 - STORAGE_DEVICE_DESCRIPTOR
 - winioctl/STORAGE_DEVICE_DESCRIPTOR
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
 - STORAGE_DEVICE_DESCRIPTOR
---

# STORAGE_DEVICE_DESCRIPTOR structure


## -description

Used in conjunction with the 
   <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> control code 
   to retrieve the storage device descriptor data for a device.

## -struct-fields

### -field Version

Contains the size of this structure, in bytes. The value of this member will change as members are added to 
      the structure.

### -field Size

Specifies the total size of the descriptor, in bytes, which may include vendor ID, product ID, product 
      revision, device serial number strings and bus-specific data which are appended to the structure.

### -field DeviceType

Specifies the device type as defined by the Small Computer Systems Interface (SCSI) specification.

### -field DeviceTypeModifier

Specifies the device type modifier, if any, as defined by the SCSI specification. If no device type 
      modifier exists, this member is zero.

### -field RemovableMedia

Indicates when <b>TRUE</b> that the device's media (if any) is removable. If the device 
      has no media, this member should be ignored. When <b>FALSE</b> the device's media is not 
      removable.

### -field CommandQueueing

Indicates when <b>TRUE</b> that the device supports multiple outstanding commands (SCSI 
      tagged queuing or equivalent). When <b>FALSE</b>, the device does not support SCSI-tagged 
      queuing or the equivalent.

### -field VendorIdOffset

Specifies the byte offset from the beginning of the structure to a null-terminated ASCII string that 
      contains the device's vendor ID. If the device has no vendor ID, this member is zero.

### -field ProductIdOffset

Specifies the byte offset from the beginning of the structure to a null-terminated ASCII string that 
      contains the device's product ID. If the device has no product ID, this member is zero.

### -field ProductRevisionOffset

Specifies the byte offset from the beginning of the structure to a null-terminated ASCII string that 
      contains the device's product revision string. If the device has no product revision string, this member is 
      zero.

### -field SerialNumberOffset

Specifies the byte offset from the beginning of the structure to a null-terminated ASCII string that 
      contains the device's serial number. If the device has no serial number, this member is zero.

### -field BusType

Specifies an enumerator value of type 
      <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_bus_type">STORAGE_BUS_TYPE</a> that indicates the type of bus to 
      which the device is connected. This should be used to interpret the raw device properties at the end of this 
      structure (if any).

### -field RawPropertiesLength

Indicates the number of bytes of bus-specific data that have been appended to this descriptor.

### -field RawDeviceProperties

Contains an array of length one that serves as a place holder for the first byte of the bus specific 
      property data.

## -remarks

An application can determine the required buffer size by issuing a 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> control code 
    passing a <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_descriptor_header">STORAGE_DESCRIPTOR_HEADER</a> structure 
    for the output buffer, and then using the returned <b>Size</b> member of the 
    <b>STORAGE_DESCRIPTOR_HEADER</b> structure to allocate 
    a buffer of the proper size.

## -see-also

<a href="/windows/desktop/FileIO/disk-management-structures">Disk Management Structures</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_adapter_descriptor">STORAGE_ADAPTER_DESCRIPTOR</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_descriptor_header">STORAGE_DESCRIPTOR_HEADER</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor">STORAGE_DEVICE_DESCRIPTOR</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_device_id_descriptor">STORAGE_DEVICE_ID_DESCRIPTOR</a>