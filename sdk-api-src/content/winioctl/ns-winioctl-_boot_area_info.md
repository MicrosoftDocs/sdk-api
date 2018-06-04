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

# _BOOT_AREA_INFO structure


## -description


Contains the output for the <a href="https://msdn.microsoft.com/library/windows/hardware/ff728858">FSCTL_GET_BOOT_AREA_INFO</a> control code.


## -struct-fields




### -field BootSectorCount

Number of elements in the <b>BootSectors</b> array.


### -field Offset

 


### -field BootSectors

A variable length array of structures each containing the following member.



#### Offset

The location of a boot sector or a copy of a boot sector.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff728858">FSCTL_GET_BOOT_AREA_INFO</a>
 

 

