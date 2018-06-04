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

# IFsrmPropertyBag::get_VolumeName


## -description


The name of the volume on which the file exists.

This property is read-only.


## -parameters


## -remarks



This property contains the volume name of the location of the file being scanned. For example, if the path to a file is "P:\folder1\subfolderA\test.txt", the volume name is "P:\".

The caller should not expect that the volume name returned will consistently have a trailing backslash.

The volume name that is returned will always be the name of a live volume. In the case where the file being classified is on a snapshot, the name of the live volume that the snapshot corresponds to will be returned.




## -see-also




<a href="https://msdn.microsoft.com/237f024d-2b1d-45d5-a63d-c530426278e6">IFsrmPropertyBag</a>
 

 

