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

# PssWalkMarkerFree function


## -description


Frees a walk marker created by <a href="https://msdn.microsoft.com/58E2FBAF-661C-45BE-A25A-A096AF52ED3E">PssWalkMarkerCreate</a>.


## -parameters




### -param WalkMarkerHandle [in]

A handle to the walk marker.


## -returns



This function returns <b>ERROR_SUCCESS</b> on success.

All error codes are defined in winerror.h. Use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.




## -remarks



If <a href="https://msdn.microsoft.com/58E2FBAF-661C-45BE-A25A-A096AF52ED3E">PssWalkMarkerCreate</a> used <b>AllocRoutine</b> of a custom allocator to create the walk marker, <b>PssWalkMarkerFree</b> uses the <b>FreeRoutine</b> of the allocator.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

