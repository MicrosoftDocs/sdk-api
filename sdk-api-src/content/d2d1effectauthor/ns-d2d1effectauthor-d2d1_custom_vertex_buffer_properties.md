---
UID: NS:d2d1effectauthor.D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES
title: D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES
author: windows-sdk-content
description: Defines a vertex shader and the input element description to define the input layout.
old-location: direct2d\d2d1_custom_vertex_buffer_properties.htm
old-project: direct2d
ms.assetid: e3cebb2b-48fb-42b2-8eb4-b9676b581bac
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES, D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES structure [Direct2D], d2d1effectauthor/D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES, direct2d.d2d1_custom_vertex_buffer_properties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1effectauthor.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effectauthor.h
api_name:
 - D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES structure


## -description


Defines a vertex shader and the input element description to define the input layout. The combination is used to allow a custom vertex effect to create a custom vertex shader and pass it a custom layout.


## -struct-fields




### -field shaderBufferWithInputSignature

 


### -field shaderBufferSize

 


### -field inputElements

An array of input assembler stage data types.


### -field elementCount

The number of input elements in the vertex shader.


### -field stride

The vertex stride.


#### - vertexShader

The unique ID of the vertex shader.


## -remarks



The vertex shader will be loaded by the <a href="https://msdn.microsoft.com/8E59527F-B6CE-4E25-B7F7-2D03BC1ACAFD">CreateVertexBuffer</a> call that accepts the vertex buffer properties.

This structure does not need to be specified if one of the standard vertex shaders is used.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh404337(v=VS.85).aspx">D2D1_VERTEX_USAGE</a>



<a href="https://msdn.microsoft.com/8E59527F-B6CE-4E25-B7F7-2D03BC1ACAFD">ID2D1EffectContext::CreateVertexBuffer</a>



<a href="https://msdn.microsoft.com/60D3DB1B-D347-44FC-98F9-545D4213F1F0">ID2D1EffectContext::LoadVertexShader</a>
 

 

