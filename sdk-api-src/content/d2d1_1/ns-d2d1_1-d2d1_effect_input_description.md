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

# D2D1_EFFECT_INPUT_DESCRIPTION structure


## -description


Describes features of an effect.


## -struct-fields




### -field effect

 


### -field inputIndex

The input index of the effect that is being considered.


### -field inputRectangle

The amount of data that would be available on the input. This can be used to query this information when the data is not yet available. 


#### - Effect

The effect whose input connection is being specified.


## -remarks



<div class="alert"><b>Note</b>  The caller should not rely heavily on the input rectangles returned by this structure. They can change due to subtle changes in effect implementations and due to optimization changes in the effect rendering system. </div>
<div> </div>


