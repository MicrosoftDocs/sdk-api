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

# DIRECTMANIPULATION_HITTEST_TYPE enumeration


## -description


Defines how hit testing is handled by <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> when using a dedicated hit-test thread registered through <a href="https://msdn.microsoft.com/ba71a959-b9b9-4466-9239-f3c486f5e7b3">RegisterHitTestTarget</a>.


## -enum-fields




### -field DIRECTMANIPULATION_HITTEST_TYPE_ASYNCHRONOUS

The hit-test thread receives <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac000">WM_POINTERDOWN</a> messages and specifies whether to call <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a>. If <b>SetContact</b> is not called, the contact will not be associated with a viewport.   


### -field DIRECTMANIPULATION_HITTEST_TYPE_SYNCHRONOUS

The UI thread always receives <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac000">WM_POINTERDOWN</a> messages after the hit-test thread. A call to <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> is not required.


### -field DIRECTMANIPULATION_HITTEST_TYPE_AUTO_SYNCHRONOUS

The UI thread receives <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac000">WM_POINTERDOWN</a> messages only when <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> isn't called by the hit-test thread.


## -see-also




<a href="https://msdn.microsoft.com/D116798F-E381-46D4-8271-8BD8CADC9D27">Direct Manipulation Enumerations</a>
 

 

