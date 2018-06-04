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

# _STORAGE_DEVICE_DESCRIPTOR structure


## -description


Used in conjunction with the 
   <a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a> control code 
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
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff566356">STORAGE_BUS_TYPE</a> that indicates the type of bus to 
      which the device is connected. This should be used to interpret the raw device properties at the end of this 
      structure (if any). 


### -field RawPropertiesLength

Indicates the number of bytes of bus-specific data that have been appended to this descriptor.


### -field RawDeviceProperties

Contains an array of length one that serves as a place holder for the first byte of the bus specific 
      property data. 


## -remarks




    An application can determine the required buffer size by issuing a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a> control code 
    passing a <a href="https://msdn.microsoft.com/library/windows/hardware/ff566968">STORAGE_DESCRIPTOR_HEADER</a> structure 
    for the output buffer, and then using the returned <b>Size</b> member of the 
    <b>STORAGE_DESCRIPTOR_HEADER</b> structure to allocate 
    a buffer of the proper size.




## -see-also




<a href="https://msdn.microsoft.com/dd55c570-68b5-4dc5-9fd0-a6e3277c318b">Disk Management Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566346">STORAGE_ADAPTER_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566968">STORAGE_DESCRIPTOR_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566971">STORAGE_DEVICE_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566972">STORAGE_DEVICE_ID_DESCRIPTOR</a>
 

 

