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

# _STORAGE_DEPENDENCY_INFO structure


## -description


Contains virtual hard disk (VHD) storage dependency information.


## -struct-fields




### -field Version

A <a href="https://msdn.microsoft.com/80437477-3f5e-4dac-a773-9339c5b742e2">STORAGE_DEPENDENCY_INFO_VERSION</a> enumeration that specifies the version of the information structure being passed to or from  the VHD functions. Can be <a href="https://msdn.microsoft.com/63296975-583d-415c-8c1f-f0cccfc5a1b3">STORAGE_DEPENDENCY_INFO_TYPE_1</a> or <a href="https://msdn.microsoft.com/f3e57773-0008-4715-9136-a9b990beea58">STORAGE_DEPENDENCY_INFO_TYPE_2</a>.


### -field NumberEntries

Number of entries returned in the following unioned members.


### -field Version1Entries

Variable-length array containing <a href="https://msdn.microsoft.com/63296975-583d-415c-8c1f-f0cccfc5a1b3">STORAGE_DEPENDENCY_INFO_TYPE_1</a> structures.


### -field Version2Entries

Variable-length array containing <a href="https://msdn.microsoft.com/f3e57773-0008-4715-9136-a9b990beea58">STORAGE_DEPENDENCY_INFO_TYPE_2</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

