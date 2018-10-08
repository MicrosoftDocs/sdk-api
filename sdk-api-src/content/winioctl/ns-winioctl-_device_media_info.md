---
UID: NS:winioctl._DEVICE_MEDIA_INFO
title: "_DEVICE_MEDIA_INFO"
author: windows-sdk-content
description: Provides information about the media supported by a device.
old-location: base\device_media_info_str.htm
tech.root: devio
ms.assetid: 90367411-3008-4e37-9884-e586fc5162d9
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: "*PDEVICE_MEDIA_INFO, DEVICE_MEDIA_INFO, DEVICE_MEDIA_INFO structure, MEDIA_CURRENTLY_MOUNTED, MEDIA_ERASEABLE, MEDIA_READ_ONLY, MEDIA_READ_WRITE, MEDIA_WRITE_ONCE, MEDIA_WRITE_PROTECTED, PDEVICE_MEDIA_INFO, PDEVICE_MEDIA_INFO structure pointer, _DEVICE_MEDIA_INFO, _win32_device_media_info_str, base.device_media_info_str, winioctl/DEVICE_MEDIA_INFO, winioctl/PDEVICE_MEDIA_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - DEVICE_MEDIA_INFO
product: Windows
targetos: Windows
req.typenames: DEVICE_MEDIA_INFO, *PDEVICE_MEDIA_INFO
req.redist: 
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
        <a href="https://msdn.microsoft.com/f584d766-0d4d-49b8-b58a-09556c494270">STORAGE_MEDIA_TYPE</a> or 
        <a href="https://msdn.microsoft.com/183cf8fc-c17b-4def-b590-0aa4b67488f6">MEDIA_TYPE</a> enumeration types.


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
        <a href="https://msdn.microsoft.com/f584d766-0d4d-49b8-b58a-09556c494270">STORAGE_MEDIA_TYPE</a> or 
        <a href="https://msdn.microsoft.com/183cf8fc-c17b-4def-b590-0aa4b67488f6">MEDIA_TYPE</a> enumeration types.


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
        <a href="https://msdn.microsoft.com/f584d766-0d4d-49b8-b58a-09556c494270">STORAGE_MEDIA_TYPE</a> or 
        <a href="https://msdn.microsoft.com/183cf8fc-c17b-4def-b590-0aa4b67488f6">MEDIA_TYPE</a> enumeration types.


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
        <a href="https://msdn.microsoft.com/fb5a17f7-8ddb-4738-83e1-f00abc3555d2">STORAGE_BUS_TYPE</a> enumeration values.


### -field DeviceSpecific.TapeInfo.BusSpecificData

A union that contains the following members.


### -field DeviceSpecific.TapeInfo.BusSpecificData.ScsiInformation

A structure that contains the following members.


### -field DeviceSpecific.TapeInfo.BusSpecificData.ScsiInformation.MediumType

The SCSI-specific medium type.


### -field DeviceSpecific.TapeInfo.BusSpecificData.ScsiInformation.DensityCode

The SCSI-specific current operating density for read/write operations.


## -see-also




<a href="https://msdn.microsoft.com/07d1ccc5-5f8a-4272-a9be-74fa7a9e1bbc">GET_MEDIA_TYPES</a>



<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>



<a href="https://msdn.microsoft.com/183cf8fc-c17b-4def-b590-0aa4b67488f6">MEDIA_TYPE</a>



<a href="https://msdn.microsoft.com/fb5a17f7-8ddb-4738-83e1-f00abc3555d2">STORAGE_BUS_TYPE</a>



<a href="https://msdn.microsoft.com/f584d766-0d4d-49b8-b58a-09556c494270">STORAGE_MEDIA_TYPE</a>
 

 

