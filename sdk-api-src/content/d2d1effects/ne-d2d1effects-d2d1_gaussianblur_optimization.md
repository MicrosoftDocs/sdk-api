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

# D2D1_GAUSSIANBLUR_OPTIMIZATION enumeration


## -description



          The optimization mode for the <a href="https://msdn.microsoft.com/6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC">Gaussian blur effect</a>.
        


## -enum-fields




### -field D2D1_GAUSSIANBLUR_OPTIMIZATION_SPEED

Applies internal optimizations such as pre-scaling at relatively small radii. Uses linear filtering.


### -field D2D1_GAUSSIANBLUR_OPTIMIZATION_BALANCED

Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.


### -field D2D1_GAUSSIANBLUR_OPTIMIZATION_QUALITY

Only uses internal optimizations with large blur radii, where approximations are less likely to be visible. Uses trilinear filtering.


### -field D2D1_GAUSSIANBLUR_OPTIMIZATION_FORCE_DWORD



