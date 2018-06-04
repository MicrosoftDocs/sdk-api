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

# MFCreateSensorProfile function


## -description


Creates a sensor profile, based on the specified type, index, and optional constraints.


## -parameters




### -param ProfileType [in]

The profile type to create.


### -param ProfileIndex [in, out]

The profile index.


### -param Constraints [in, optional]

Any optional constraints to be put on the profile.


### -param ppProfile [out]

On success, returns a double pointer to the <a href="https://msdn.microsoft.com/58D9FE3F-0F42-4262-B1BE-336BFA2E4BC7">IMFSensorProfile</a> containing the sensor profile.


## -returns



This function does not return a value.



