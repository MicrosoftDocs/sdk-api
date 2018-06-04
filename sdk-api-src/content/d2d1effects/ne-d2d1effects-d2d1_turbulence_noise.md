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

# D2D1_TURBULENCE_NOISE enumeration


## -description


The turbulence noise mode for the <a href="https://msdn.microsoft.com/86C1990E-958C-46D7-840A-E4A17F1D1740">Turbulence effect</a>. 
        Indicates whether to generate a bitmap based on Fractal Noise or the Turbulence function. 


## -enum-fields




### -field D2D1_TURBULENCE_NOISE_FRACTAL_SUM

Computes a sum of the octaves, shifting the output range from [-1, 1], to [0, 1]. 


### -field D2D1_TURBULENCE_NOISE_TURBULENCE

Computes a sum of the absolute value of each octave.


### -field D2D1_TURBULENCE_NOISE_FORCE_DWORD



