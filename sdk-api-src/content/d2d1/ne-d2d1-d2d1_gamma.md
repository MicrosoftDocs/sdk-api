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

# D2D1_GAMMA enumeration


## -description


Specifies which gamma is used for interpolation.


## -enum-fields




### -field D2D1_GAMMA_2_2

Interpolation is performed in the standard RGB (sRGB) gamma.


### -field D2D1_GAMMA_1_0

Interpolation is performed in the linear-gamma color space.


### -field D2D1_GAMMA_FORCE_DWORD




## -remarks



Interpolating in a linear gamma space (<b>D2D1_GAMMA_1_0</b>) can avoid changes in perceived brightness caused by the effect of gamma correction in spaces where the gamma is not 1.0, such as the default sRGB color space, where the gamma is 2.2. For an example of the differences between these two blending modes, consider the following illustration, which shows two gradients, each of which blends from red to blue to green:

<img alt="Illustration of two gradients from red to blue to green, blended by using sRGB gamma and linear-gamma" src="images/D2D1_GAMMA.png"/>

The first gradient is interpolated linearly in the space of the render target (sRGB in this case), and one can see the dark bands between each color. The second gradient uses a gamma-correct linear interpolation, and thus does not exhibit the same variations in brightness.



