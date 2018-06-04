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

# _ENUM_PAGE_FILE_INFORMATION structure


## -description


Contains information about a pagefile.


## -struct-fields




### -field cb

The size of this structure, in bytes.


### -field Reserved

This member is reserved.


### -field TotalSize

The total size of the pagefile, in pages.


### -field TotalInUse

The current pagefile usage, in pages.


### -field PeakUsage

The peak pagefile usage, in pages.


## -see-also




<a href="https://msdn.microsoft.com/eb3610fb-2c95-4f7b-973d-8dc41d2829f1">EnumPageFilesProc</a>
 

 

