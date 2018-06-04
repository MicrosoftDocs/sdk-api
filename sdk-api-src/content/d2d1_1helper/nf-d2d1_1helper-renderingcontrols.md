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

# RenderingControls function


## -description


Returns a filled D2D1_RENDERING_CONTROLS structure.


## -parameters




### -param bufferPrecision

Type: <b><a href="https://msdn.microsoft.com/a2a4b4fd-685d-4068-b1f5-609e6ab024e2">D2D1_BUFFER_PRECISION</a></b>

The buffer precision used by default if the buffer precision is not otherwise specified by the effect or the transform.


### -param tileSize

Type: <b><a href="https://msdn.microsoft.com/e28da5ee-7d68-4ec5-b477-c6ead0c725e6">D2D1_SIZE_U</a></b>

The minimum tile allocation size to be used by the imaging effect renderer.


## -returns



Type: <b><a href="https://msdn.microsoft.com/e563cbb0-2ee0-43d8-978c-0bde1950a926">D2D1_RENDERING_CONTROLS</a></b>

Describes limitations to be applied to an imaging effect renderer.



