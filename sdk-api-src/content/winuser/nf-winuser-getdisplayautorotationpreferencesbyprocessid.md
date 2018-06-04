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

# GetDisplayAutoRotationPreferencesByProcessId function


## -description


Retrieves the screen auto-rotation preferences for the process indicated by the <i>dwProcessId</i> parameter.


## -parameters




### -param dwProcessId [in]

The process to get preference settings for.


### -param pOrientation [out]

Pointer to a location in memory that will receive the current orientation preference setting for the indicated process.


### -param fRotateScreen [out]

Pointer to a location in memory that will receive a TRUE or FALSE value indicating whether the screen was rotated to comply with the process orientation preferences.


## -returns



TRUE if the method succeeds, otherwise FALSE.

Applications should use <a href="https://msdn.microsoft.com/48D609CC-3E2B-4E0E-9566-FE02853DD831">GetDisplayAutoRotationPreferences</a> to retrieve their auto-rotation preferences instead of using this API. For an example, see <a href="https://msdn.microsoft.com/48D609CC-3E2B-4E0E-9566-FE02853DD831">GetDisplayAutoRotationPreferences</a>.



