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

# RO_INIT_TYPE enumeration


## -description


Determines the concurrency model used for incoming calls to the objects created by this thread.


## -enum-fields




### -field RO_INIT_SINGLETHREADED


### -field RO_INIT_MULTITHREADED

Initializes the thread for multi-threaded concurrency. The current thread is initialized in the MTA.


## -remarks



Pass the <b>RO_INIT_TYPE</b> enumeration to the <a href="https://msdn.microsoft.com/527A7FF7-749D-4178-A397-5C538F6031F8">RoInitialize</a> function to initialize a thread in the Windows Runtime.




## -see-also




<a href="https://msdn.microsoft.com/527A7FF7-749D-4178-A397-5C538F6031F8">RoInitialize</a>
 

 

