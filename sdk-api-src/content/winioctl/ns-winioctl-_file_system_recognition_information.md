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

# _FILE_SYSTEM_RECOGNITION_INFORMATION structure


## -description


Contains file system recognition information retrieved by the <a href="https://msdn.microsoft.com/0b2ff131-a659-4bd0-b329-41fb60edbe13">FSCTL_QUERY_FILE_SYSTEM_RECOGNITION</a> control code.


## -struct-fields




### -field FileSystem

The file system name stored on the disk. This is a null-terminated string of 8 ASCII characters that represents the nonlocalizable human-readable name of the 
    file system the volume is formatted with.


## -see-also




<a href="https://msdn.microsoft.com/d9c19e01-ff82-4bbc-9eb6-aac9dc5c34ac">FILE_SYSTEM_RECOGNITION_STRUCTURE</a>



<a href="https://msdn.microsoft.com/0b2ff131-a659-4bd0-b329-41fb60edbe13">FSCTL_QUERY_FILE_SYSTEM_RECOGNITION</a>
 

 

