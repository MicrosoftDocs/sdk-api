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

# STARTING_VCN_INPUT_BUFFER structure


## -description


Contains the starting VCN to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff545421">FSCTL_GET_RETRIEVAL_POINTERS</a> control code.


## -struct-fields




### -field StartingVcn

The VCN at which 
the operation will begin enumerating extents in the file. This value may be rounded down to the first VCN of the extent in which the specified extent is found.


## -see-also




<a href="https://msdn.microsoft.com/a35dbd6e-1344-4694-9760-7bc3d33196e5">Defragmentation</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545421">FSCTL_GET_RETRIEVAL_POINTERS</a>
 

 

