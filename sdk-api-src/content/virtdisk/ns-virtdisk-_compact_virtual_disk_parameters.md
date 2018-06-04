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

# _COMPACT_VIRTUAL_DISK_PARAMETERS structure


## -description


Contains virtual hard disk (VHD)  compacting parameters.


## -struct-fields




### -field Version

A <a href="https://msdn.microsoft.com/79b8088a-8e30-44c8-8227-82eb1c03e77c">COMPACT_VIRTUAL_DISK_VERSION</a> 
     enumeration that specifies the version of the 
     <b>COMPACT_VIRTUAL_DISK_PARAMETERS</b> 
     structure being passed to or from the VHD functions.


### -field Version1

A structure with the following member.


### -field Version1.Reserved

Reserved. Must be set to zero.


## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

