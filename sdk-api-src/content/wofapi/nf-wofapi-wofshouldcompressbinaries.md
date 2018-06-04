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

# WofShouldCompressBinaries function


## -description


Indicates whether compression should be used on a particular volume, and if so, which compression algorithm should be used. 



## -parameters




### -param Volume [in]

Specifies the path to the volume whose compression state is desired. 


### -param Algorithm [out]

Points to a ULONG value. If the function returns TRUE, indicating compression is desired, this value will contain the algorithm that should be used for this volume. 



## -returns



If binaries on this volume should be compressed, the return value is TRUE; otherwise it is FALSE. This function will return FALSE if the system does not support compression on the specified volume. 





