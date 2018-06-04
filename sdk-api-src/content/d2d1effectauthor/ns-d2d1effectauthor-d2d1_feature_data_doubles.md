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

# D2D1_FEATURE_DATA_DOUBLES structure


## -description


Describes the support for doubles in shaders.


## -struct-fields




### -field doublePrecisionFloatShaderOps

TRUE is doubles are supported within the shaders.


## -remarks



Fill this structure by passing a D2D1_FEATURE_DOUBLES structure to <a href="https://msdn.microsoft.com/1A97B928-7715-4D4E-AD38-7D01EE243494">ID2D1EffectContext::CheckFeatureSupport</a>.



