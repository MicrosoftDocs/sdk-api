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

# _VDS_DRIVE_LETTER_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of a drive letter.


## -struct-fields




### -field wcLetter

The drive letter.


### -field volumeId

The GUID of the volume object represented by the drive letter. 


### -field ulFlags

The drive letter flags enumerated by <a href="https://msdn.microsoft.com/f6eebe08-ebc9-45d3-a752-9cdc13f9bcf1">VDS_DRIVE_LETTER_FLAG</a>.


### -field bUsed

If true, the drive letter is already in use; otherwise, the drive letter is available.


## -remarks



The <a href="https://msdn.microsoft.com/e9e9f8b0-963f-4c57-9553-8b9241317b55">IVdsService::QueryDriveLetters</a> method returns this structure to report the property details of a drive letter.




## -see-also




<a href="https://msdn.microsoft.com/e9e9f8b0-963f-4c57-9553-8b9241317b55">IVdsService::QueryDriveLetters</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/f6eebe08-ebc9-45d3-a752-9cdc13f9bcf1">VDS_DRIVE_LETTER_FLAG</a>
 

 

