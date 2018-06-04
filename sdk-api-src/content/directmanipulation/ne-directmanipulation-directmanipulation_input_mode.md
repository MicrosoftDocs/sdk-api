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

# DIRECTMANIPULATION_INPUT_MODE enumeration


## -description


Defines the threading behavior for <a href="https://msdn.microsoft.com/2be1c8a1-a729-4851-b103-b108b9a96e2d">SetInputMode</a> or <a href="https://msdn.microsoft.com/10516474-f3ef-4de7-a5b5-aabaa5c65cf5">SetUpdateMode</a>. The exact meaning of each constant depends on the method called.


## -enum-fields




### -field DIRECTMANIPULATION_INPUT_MODE_AUTOMATIC

Input is automatically passed to the viewport in an independent thread.


### -field DIRECTMANIPULATION_INPUT_MODE_MANUAL

Input is manually passed by   the app on its thread via the <a href="https://msdn.microsoft.com/ed7fa19b-acfe-4d5d-bd71-a77e5016fe68">ProcessInput</a> method.


## -see-also




<a href="https://msdn.microsoft.com/D116798F-E381-46D4-8271-8BD8CADC9D27">Direct Manipulation Enumerations</a>
 

 

