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

# D2D1_VERTEX_BUFFER_PROPERTIES structure


## -description


Defines the properties of a vertex buffer that are standard for all vertex shader definitions.


## -struct-fields




### -field inputCount

The number of inputs to the vertex shader.


### -field usage

Indicates how frequently the vertex buffer is likely to be updated.


### -field data

The initial contents of the vertex buffer.


### -field byteWidth

The size of the vertex buffer, in bytes.


## -remarks



If <b>usage</b> is dynamic, the system might return a system memory buffer and copy these vertices into the rendering vertex buffer for each element.

If the initialization data is not specified, the buffer will be uninitialized.




## -see-also




<a href="https://msdn.microsoft.com/ff122e0d-5f0e-4a61-bead-53bea6f1648f">D2D1_VERTEX_USAGE</a>



<a href="https://msdn.microsoft.com/8E59527F-B6CE-4E25-B7F7-2D03BC1ACAFD">ID2D1EffectContext::CreateVertexBuffer</a>



<a href="https://msdn.microsoft.com/60D3DB1B-D347-44FC-98F9-545D4213F1F0">ID2D1EffectContext::LoadVertexShader</a>
 

 

