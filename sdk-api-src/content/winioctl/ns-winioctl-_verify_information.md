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

# _VERIFY_INFORMATION structure


## -description


Contains information used to verify a disk extent. It is the output buffer for the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560420">IOCTL_DISK_VERIFY</a> control code.


## -struct-fields




### -field StartingOffset

The starting offset of the disk extent. 


### -field Length

The length of the disk extent, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff560420">IOCTL_DISK_VERIFY</a>
 

 

