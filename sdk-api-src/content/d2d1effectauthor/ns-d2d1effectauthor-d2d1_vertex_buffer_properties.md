---
UID: NS:d2d1effectauthor.D2D1_VERTEX_BUFFER_PROPERTIES
title: D2D1_VERTEX_BUFFER_PROPERTIES
author: windows-sdk-content
description: Defines the properties of a vertex buffer that are standard for all vertex shader definitions.
old-location: direct2d\d2d1_vertex_buffer_properties.htm
tech.root: direct2d
ms.assetid: d2f46c31-10f3-4318-8185-40a6bbd8ef8a
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: D2D1_VERTEX_BUFFER_PROPERTIES, D2D1_VERTEX_BUFFER_PROPERTIES structure [Direct2D], d2d1effectauthor/D2D1_VERTEX_BUFFER_PROPERTIES, direct2d.d2d1_vertex_buffer_properties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2d1.lib; D2d1.dll
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_VERTEX_BUFFER_PROPERTIES
product: Windows
targetos: Windows
req.typenames: D2D1_VERTEX_BUFFER_PROPERTIES
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Hh404337(v=VS.85).aspx">D2D1_VERTEX_USAGE</a>



<a href="https://msdn.microsoft.com/8E59527F-B6CE-4E25-B7F7-2D03BC1ACAFD">ID2D1EffectContext::CreateVertexBuffer</a>



<a href="https://msdn.microsoft.com/60D3DB1B-D347-44FC-98F9-545D4213F1F0">ID2D1EffectContext::LoadVertexShader</a>
 

 

