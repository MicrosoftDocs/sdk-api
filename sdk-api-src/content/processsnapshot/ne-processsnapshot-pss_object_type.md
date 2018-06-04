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

# PSS_OBJECT_TYPE enumeration


## -description


Specifies the object type in a <a href="https://msdn.microsoft.com/F56E8C35-949A-4DEE-973F-CF24F6596036">PSS_HANDLE_ENTRY</a> structure.


## -enum-fields




### -field PSS_OBJECT_TYPE_UNKNOWN

The object type is either unknown or unsupported.


### -field PSS_OBJECT_TYPE_PROCESS

The object is a process.


### -field PSS_OBJECT_TYPE_THREAD

The object is a thread. 


### -field PSS_OBJECT_TYPE_MUTANT

The object is a mutant/mutex.


### -field PSS_OBJECT_TYPE_EVENT

The object is an event.


### -field PSS_OBJECT_TYPE_SECTION

The object is a file-mapping object.


### -field PSS_OBJECT_TYPE_SEMAPHORE




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

