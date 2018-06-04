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

# GetAutoRotationState function


## -description


Retrieves an <a href="https://msdn.microsoft.com/55BCB2EB-524D-478A-8DCE-53E59DD0822D">AR_STATE</a> value containing the state of screen auto-rotation for the system, for example whether auto-rotation is supported, and whether it is enabled by the user. <b>GetAutoRotationState</b> provides a robust and diverse way of querying for auto-rotation state, and more. For example, if you want your app to behave differently when multiple monitors are attached then you can determine that from the <b>AR_STATE</b> returned.


## -parameters




### -param pState [out]

Pointer to a location in memory that will receive the current state of auto-rotation for the system.


## -returns



TRUE if the method succeeds, otherwise FALSE.

See <a href="https://msdn.microsoft.com/48D609CC-3E2B-4E0E-9566-FE02853DD831">GetDisplayAutoRotationPreferences</a> for an example of using this function.



