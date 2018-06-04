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

# D2D1_THREADING_MODE enumeration


## -description


Specifies the threading mode used while simultaneously creating the device, factory, and device context.



## -enum-fields




### -field D2D1_THREADING_MODE_SINGLE_THREADED

Resources may only be invoked serially.  Device context state is not protected from multi-threaded access. 


### -field D2D1_THREADING_MODE_MULTI_THREADED

Resources may be invoked from multiple threads. Resources use interlocked reference counting and their state is protected.



### -field D2D1_THREADING_MODE_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/657439fe-dc17-42af-9e2c-2f3cb769a5a3">D2D1_CREATION_PROPERTIES</a>



<a href="https://msdn.microsoft.com/FDD770D4-817F-44D9-86C4-15DD04D214AE">Multithreaded Direct2D Apps</a>
 

 

