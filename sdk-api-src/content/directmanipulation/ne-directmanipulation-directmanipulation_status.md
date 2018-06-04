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

# DIRECTMANIPULATION_STATUS enumeration


## -description


Defines the possible states of <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a>. The viewport can process input in any state unless otherwise noted.


## -enum-fields




### -field DIRECTMANIPULATION_BUILDING

The viewport is being initialized and is not yet able to process input.


### -field DIRECTMANIPULATION_ENABLED

The viewport was successfully enabled.


### -field DIRECTMANIPULATION_DISABLED

The viewport is disabled and cannot process input or callbacks. The viewport can be enabled by calling <a href="https://msdn.microsoft.com/library/windows/hardware/hh451004">Enable</a>.


### -field DIRECTMANIPULATION_RUNNING

The viewport is currently processing input and updating content.


### -field DIRECTMANIPULATION_INERTIA

The viewport is moving content due to inertia.


### -field DIRECTMANIPULATION_READY

The viewport has completed the previous interaction. 


### -field DIRECTMANIPULATION_SUSPENDED

The transient state of the viewport when input has been promoted to an ancestor in the <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> chain.


## -see-also




<a href="https://msdn.microsoft.com/D116798F-E381-46D4-8271-8BD8CADC9D27">Direct Manipulation Enumerations</a>
 

 

