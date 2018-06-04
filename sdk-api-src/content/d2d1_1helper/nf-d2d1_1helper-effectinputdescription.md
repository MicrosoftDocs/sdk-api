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

# EffectInputDescription function


## -description


Creates a <a href="https://msdn.microsoft.com/2ce9405a-e36d-4b9e-b9d2-2a58b78696ac">D2D1_EFFECT_INPUT_DESCRIPTION</a> structure.


## -parameters




### -param effect

Type: <b><a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>*</b>

The effect whose input connection is being specified.


### -param inputIndex

Type: <b>UINT32</b>

The input index of the effect that is being considered.


### -param inputRectangle

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

The amount of data that would be available on the input. This can be used to query this information when the data is not yet available. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/2ce9405a-e36d-4b9e-b9d2-2a58b78696ac">D2D1_EFFECT_INPUT_DESCRIPTION</a></b>

The filled description structure that describes the input to the effect.



