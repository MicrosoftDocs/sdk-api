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

# D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS structure


## -description


Describes compute shader support, which is an option on D3D10 feature level.


## -struct-fields




### -field computeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x

Shader model 4 compute shaders are supported.


## -remarks



You can fill this structure by passing a D2D1_ FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS structure to <a href="https://msdn.microsoft.com/1A97B928-7715-4D4E-AD38-7D01EE243494">ID2D1EffectContext::CheckFeatureSupport</a>.



