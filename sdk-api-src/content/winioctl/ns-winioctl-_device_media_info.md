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

# _DEVICE_MEDIA_INFO structure


## -description


Provides information about the media supported by a device.


## -struct-fields




### -field DeviceSpecific

A union that contains the following members.


### -field DeviceSpecific.DiskInfo

A structure that contains the following members.


### -field DeviceSpecific.DiskInfo.Cylinders

The number of cylinders on this disk.


### -field DeviceSpecific.DiskInfo.MediaType

The media type. This member can be one of the values from the 
        <a href="https://msdn.microsoft.com/library/windows/hardware/ff566992">STORAGE_MEDIA_TYPE</a> or 
        <a href="https://msdn.microsoft.com/library/windows/hardware/ff562216">MEDIA_TYPE</a> enumeration types.


### -field DeviceSpecific.DiskInfo.TracksPerCylinder

The number of tracks per cylinder.


### -field DeviceSpecific.DiskInfo.SectorsPerTrack

The number of sectors per track.


### -field DeviceSpecific.DiskInfo.BytesPerSector

The number of bytes per sector.


### -field DeviceSpecific.DiskInfo.NumberMediaSides

The number of sides of the disk that can contain data. This member is 1 for one-sided media or 2 for 
        two-sided media.


### -field DeviceSpecific.DiskInfo.MediaCharacteristics

The characteristics of the media. This member can be one or more of the following values.



###### DiskInfo.MediaCharacteristics.MEDIA_CURRENTLY_MOUNTED (0x80000000)



###### DiskInfo.MediaCharacteristics.MEDIA_ERASEABLE (0x00000001)



###### DiskInfo.MediaCharacteristics.MEDIA_READ_ONLY (0x00000004)



###### DiskInfo.MediaCharacteristics.MEDIA_READ_WRITE (0x00000008)



###### DiskInfo.MediaCharacteristics.MEDIA_WRITE_ONCE (0x00000002)



###### DiskInfo.MediaCharacteristics.MEDIA_WRITE_PROTECTED (0x00000100)


### -field DeviceSpecific.RemovableDiskInfo

A structure that contains the following members.


### -field DeviceSpecific.RemovableDiskInfo.Cylinders

The number of cylinders on this disk.


### -field DeviceSpecific.RemovableDiskInfo.MediaType

The media type. This member can be one of the values from the 
        <a href="https://msdn.microsoft.com/library/windows/hardware/ff566992">STORAGE_MEDIA_TYPE</a> or 
        <a href="https://msdn.microsoft.com/library/windows/hardware/ff562216">MEDIA_TYPE</a> enumeration types.


### -field DeviceSpecific.RemovableDiskInfo.TracksPerCylinder

The number of tracks per cylinder.


### -field DeviceSpecific.RemovableDiskInfo.SectorsPerTrack

The number of sectors per track.


### -field DeviceSpecific.RemovableDiskInfo.BytesPerSector

The number of bytes per sector.


### -field DeviceSpecific.RemovableDiskInfo.NumberMediaSides

The number of sides of the disk that can contain data. This member is 1 for one-sided media or 2 for 
        two-sided media.


### -field DeviceSpecific.RemovableDiskInfo.MediaCharacteristics

The characteristics of the media. This member can be one or more of the following values.



###### RemovableDiskInfo.MediaCharacteristics.MEDIA_CURRENTLY_MOUNTED (0x80000000)



###### RemovableDiskInfo.MediaCharacteristics.MEDIA_ERASEABLE (0x00000001)



###### RemovableDiskInfo.MediaCharacteristics.MEDIA_READ_ONLY (0x00000004)



###### RemovableDiskInfo.MediaCharacteristics.MEDIA_READ_WRITE (0x00000008)



###### RemovableDiskInfo.MediaCharacteristics.MEDIA_WRITE_ONCE (0x00000002)



###### RemovableDiskInfo.MediaCharacteristics.MEDIA_WRITE_PROTECTED (0x00000100)


### -field DeviceSpecific.TapeInfo

A structure that contains the following members.
      


### -field DeviceSpecific.TapeInfo.MediaType

The media type. This member can be one of the values from the 
        <a href="https://msdn.microsoft.com/library/windows/hardware/ff566992">STORAGE_MEDIA_TYPE</a> or 
        <a href="https://msdn.microsoft.com/library/windows/hardware/ff562216">MEDIA_TYPE</a> enumeration types.


### -field DeviceSpecific.TapeInfo.MediaCharacteristics

The characteristics of the media. This member can be one or more of the following values.



###### TapeInfo.MediaCharacteristics.MEDIA_CURRENTLY_MOUNTED (0x80000000)



###### TapeInfo.MediaCharacteristics.MEDIA_ERASEABLE (0x00000001)



###### TapeInfo.MediaCharacteristics.MEDIA_READ_ONLY (0x00000004)



###### TapeInfo.MediaCharacteristics.MEDIA_READ_WRITE (0x00000008)



###### TapeInfo.MediaCharacteristics.MEDIA_WRITE_ONCE (0x00000002)



###### TapeInfo.MediaCharacteristics.MEDIA_WRITE_PROTECTED (0x00000100)


### -field DeviceSpecific.TapeInfo.CurrentBlockSize

The current block size, in bytes.


### -field DeviceSpecific.TapeInfo.BusType

The type of bus to which the tape drive is connected. This members can be one of the 
        <a href="https://msdn.microsoft.com/library/windows/hardware/ff566356">STORAGE_BUS_TYPE</a> enumeration values.


### -field DeviceSpecific.TapeInfo.BusSpecificData

A union that contains the following members.


### -field DeviceSpecific.TapeInfo.BusSpecificData.ScsiInformation

A structure that contains the following members.


### -field DeviceSpecific.TapeInfo.BusSpecificData.ScsiInformation.MediumType

The SCSI-specific medium type.


### -field DeviceSpecific.TapeInfo.BusSpecificData.ScsiInformation.DensityCode

The SCSI-specific current operating density for read/write operations.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff554987">GET_MEDIA_TYPES</a>



<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff562216">MEDIA_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566356">STORAGE_BUS_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566992">STORAGE_MEDIA_TYPE</a>
 

 

