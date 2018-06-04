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

# _EXPAND_VIRTUAL_DISK_PARAMETERS structure


## -description


Contains virtual disk expansion request parameters.


## -struct-fields




### -field Version

An <a href="https://msdn.microsoft.com/28651993-81ad-4dfc-9c8b-3768fab5d3ae">EXPAND_VIRTUAL_DISK_VERSION</a> 
      enumeration value that specifies the version of the 
      <b>EXPAND_VIRTUAL_DISK_PARAMETERS</b> structure 
      being passed to or from the virtual disk functions.


### -field Version1

This structure is used if the <b>Version</b> member is 
       <b>EXPAND_VIRTUAL_DISK_VERSION_1</b> (1).


### -field Version1.NewSize

New size, in bytes, for the expansion request.


## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

