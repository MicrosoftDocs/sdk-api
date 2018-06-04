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

# FIND_BY_SID_OUTPUT structure


## -description


Represents a file name.


## -struct-fields




### -field NextEntryOffset

 


### -field FileIndex

 


### -field FileNameLength

The size of the file name, in bytes. This size does not include the NULL character.


### -field FileName

A pointer to a null-terminated string that specifies the file name.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544833">FSCTL_FIND_FILES_BY_SID</a>
 

 

