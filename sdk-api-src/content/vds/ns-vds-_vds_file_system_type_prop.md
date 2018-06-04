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

# _VDS_FILE_SYSTEM_TYPE_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of a file system type.


## -struct-fields




### -field type

The file system types enumerated by <a href="https://msdn.microsoft.com/56f2d969-eb1c-44c2-8a12-077a02ae40dc">VDS_FILE_SYSTEM_TYPE</a>. Valid types are FAT, FAT32, NTFS, CDFS and UDF.


### -field wszName

 The file system name.


### -field ulFlags

The file system flags enumerated by <a href="https://msdn.microsoft.com/2598877b-03f0-4190-8dcc-41ea3cb9497f">VDS_FILE_SYSTEM_FLAG</a>.


### -field ulCompressionFlags

The valid allocation unit sizes used for compression.


### -field ulMaxLableLength

The maximum length for a label name.


### -field pwszIllegalLabelCharSet

A string containing all characters that are not valid for this file system type.


## -remarks



The <a href="https://msdn.microsoft.com/17dcafc8-8faf-4dc2-af24-7e1ab257201e">IVdsService::QueryFileSystemTypes</a>
      method returns this structure to report the property details of a file-system type.




## -see-also




<a href="https://msdn.microsoft.com/17dcafc8-8faf-4dc2-af24-7e1ab257201e">IVdsService::QueryFileSystemTypes</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/2598877b-03f0-4190-8dcc-41ea3cb9497f">VDS_FILE_SYSTEM_FLAG</a>



<a href="https://msdn.microsoft.com/56f2d969-eb1c-44c2-8a12-077a02ae40dc">VDS_FILE_SYSTEM_TYPE</a>
 

 

