---
UID: NS:winioctl._STORAGE_TEMPERATURE_DATA_DESCRIPTOR
title: "_STORAGE_TEMPERATURE_DATA_DESCRIPTOR"
author: windows-sdk-content
description: This structure is used in conjunction with IOCTL_STORAGE_QUERY_PROPERTY to return temperature data from a storage device or adapter.
old-location: fs\storage_temperature_data_descriptor.htm
old-project: FileIO
ms.assetid: E155B31F-6543-42E3-BCAB-B1B0100D23E4
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR, PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR, PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR structure pointer [Files], STORAGE_TEMPERATURE_DATA_DESCRIPTOR, STORAGE_TEMPERATURE_DATA_DESCRIPTOR structure [Files], _STORAGE_TEMPERATURE_DATA_DESCRIPTOR, fs.storage_temperature_data_descriptor, winioctl/PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR, winioctl/STORAGE_TEMPERATURE_DATA_DESCRIPTOR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STORAGE_TEMPERATURE_DATA_DESCRIPTOR, *PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoctl.h
api_name:
-	STORAGE_TEMPERATURE_DATA_DESCRIPTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _STORAGE_TEMPERATURE_DATA_DESCRIPTOR structure


## -description


This structure is used in conjunction with <a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a> to return temperature data from a storage device or adapter. 


## -struct-fields




### -field Version

Contains the size of this structure, in bytes. The value of this member will change as members are added to the structure.


### -field Size

Specifies the total size of the data returned, in bytes. This may include data that follows this structure.


### -field CriticalTemperature

Indicates the minimum temperature in degrees Celsius that may prevent normal operation. Exceeding this temperature may result in possible data loss, automatic device shutdown, extreme performance throttling, or permanent damage.      


### -field WarningTemperature

Indicates the maximum temperature in degrees Celsius at which the device is capable of operating continuously without degrading operation or reliability.    


### -field InfoCount

Specifies the number of <a href="https://msdn.microsoft.com/library/windows/hardware/mt651018">STORAGE_TEMPERATURE_INFO</a> structures reported in <b>TemperatureInfo</b>. More than one set of temperature data may be returned when there are multiple sensors in the drive.


### -field Reserved0

Reserved for future use.


### -field Reserved1

Reserved for future use.


### -field TemperatureInfo

 




#### - TemperatureInfo[ANYSIZE_ARRAY]

Device temperature data, of type <a href="https://msdn.microsoft.com/library/windows/hardware/mt651018">STORAGE_TEMPERATURE_INFO</a>.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt650982">IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566996">STORAGE_PROPERTY_ID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566997">STORAGE_PROPERTY_QUERY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt651018">STORAGE_TEMPERATURE_INFO</a>
 

 

