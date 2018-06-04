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

# _VDS_FILE_SYSTEM_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of a file system.


## -struct-fields




### -field type

The file-system type enumerated by  <a href="https://msdn.microsoft.com/56f2d969-eb1c-44c2-8a12-077a02ae40dc">VDS_FILE_SYSTEM_TYPE</a>.


### -field volumeId

The GUID of the volume object containing the file system.


### -field ulFlags

The file-system flags enumerated by <a href="https://msdn.microsoft.com/f2776ee9-4809-4f99-b464-80b5b53f8675">VDS_FILE_SYSTEM_PROP_FLAG</a>.


### -field ullTotalAllocationUnits

The total number of allocation units.


### -field ullAvailableAllocationUnits

The  unused allocation units.


### -field ulAllocationUnitSize

The allocation unit size, in bytes, for the file system, which is
usually between 512 and 4096.


### -field pwszLabel

A string containing the file-system label.


## -remarks



The <a href="https://msdn.microsoft.com/43f5495c-5a60-44fd-b217-16464c4693a4">IVdsVolumeMF::GetFileSystemProperties</a>
      method returns this structure to report the property details of a file system.




## -see-also




<a href="https://msdn.microsoft.com/43f5495c-5a60-44fd-b217-16464c4693a4">IVdsVolumeMF::GetFileSystemProperties</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/f2776ee9-4809-4f99-b464-80b5b53f8675">VDS_FILE_SYSTEM_PROP_FLAG</a>



<a href="https://msdn.microsoft.com/56f2d969-eb1c-44c2-8a12-077a02ae40dc">VDS_FILE_SYSTEM_TYPE</a>
 

 

