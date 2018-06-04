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

# _D3D_SHADER_VARIABLE_TYPE enumeration


## -description


Values that identify various data, texture, and buffer types that can be assigned to a shader variable.


## -enum-fields




### -field D3D_SVT_VOID

The variable is a void pointer.


### -field D3D_SVT_BOOL

The variable is a boolean.


### -field D3D_SVT_INT

The variable is an integer.


### -field D3D_SVT_FLOAT

The variable is a floating-point number.


### -field D3D_SVT_STRING

The variable is a string.


### -field D3D_SVT_TEXTURE

The variable is a texture.


### -field D3D_SVT_TEXTURE1D

The variable is a 1D texture.


### -field D3D_SVT_TEXTURE2D

The variable is a 2D texture.


### -field D3D_SVT_TEXTURE3D

The variable is a 3D texture.


### -field D3D_SVT_TEXTURECUBE

The variable is a texture cube.


### -field D3D_SVT_SAMPLER

The variable is a sampler.


### -field D3D_SVT_SAMPLER1D


            The variable is a 1D sampler.
          


### -field D3D_SVT_SAMPLER2D


            The variable is a 2D sampler.
          


### -field D3D_SVT_SAMPLER3D


            The variable is a 3D sampler.
          


### -field D3D_SVT_SAMPLERCUBE


            The variable is a cube sampler.
          


### -field D3D_SVT_PIXELSHADER

The variable is a pixel shader.


### -field D3D_SVT_VERTEXSHADER

The variable is a vertex shader.


### -field D3D_SVT_PIXELFRAGMENT


            The variable is a pixel fragment.
          


### -field D3D_SVT_VERTEXFRAGMENT


            The variable is a vertex fragment.
          


### -field D3D_SVT_UINT

The variable is an unsigned integer.


### -field D3D_SVT_UINT8

The variable is an 8-bit unsigned integer.


### -field D3D_SVT_GEOMETRYSHADER

The variable is a geometry shader.


### -field D3D_SVT_RASTERIZER

The variable is a rasterizer-state object.


### -field D3D_SVT_DEPTHSTENCIL

The variable is a depth-stencil-state object.


### -field D3D_SVT_BLEND

The variable is a blend-state object.


### -field D3D_SVT_BUFFER

The variable is a buffer.


### -field D3D_SVT_CBUFFER

The variable is a constant buffer.


### -field D3D_SVT_TBUFFER

The variable is a texture buffer.


### -field D3D_SVT_TEXTURE1DARRAY

The variable is a 1D-texture array.


### -field D3D_SVT_TEXTURE2DARRAY

The variable is a 2D-texture array.


### -field D3D_SVT_RENDERTARGETVIEW

The variable is a render-target view.


### -field D3D_SVT_DEPTHSTENCILVIEW

The variable is a depth-stencil view.


### -field D3D_SVT_TEXTURE2DMS

The variable is a 2D-multisampled texture.


### -field D3D_SVT_TEXTURE2DMSARRAY

The variable is a 2D-multisampled-texture array.


### -field D3D_SVT_TEXTURECUBEARRAY

The variable is a texture-cube array.


### -field D3D_SVT_HULLSHADER

The variable holds a compiled hull-shader binary.


### -field D3D_SVT_DOMAINSHADER

The variable holds a compiled domain-shader binary.


### -field D3D_SVT_INTERFACE_POINTER

The variable is an interface.


### -field D3D_SVT_COMPUTESHADER

The variable holds a compiled compute-shader binary.


### -field D3D_SVT_DOUBLE

The variable is a double precision (64-bit) floating-point number.


### -field D3D_SVT_RWTEXTURE1D

The variable is a 1D read-and-write texture.


### -field D3D_SVT_RWTEXTURE1DARRAY

The variable is an array of 1D read-and-write textures.


### -field D3D_SVT_RWTEXTURE2D

The variable is a 2D read-and-write texture.


### -field D3D_SVT_RWTEXTURE2DARRAY

The variable is an array of 2D read-and-write textures.


### -field D3D_SVT_RWTEXTURE3D

The variable is a 3D read-and-write texture.


### -field D3D_SVT_RWBUFFER

The variable is a read-and-write buffer.


### -field D3D_SVT_BYTEADDRESS_BUFFER

The variable is a byte-address buffer.


### -field D3D_SVT_RWBYTEADDRESS_BUFFER

The variable is a read-and-write byte-address buffer.


### -field D3D_SVT_STRUCTURED_BUFFER

The variable is a structured buffer. 


              For more information about structured buffer, see the <b>Remarks</b> section.
            


### -field D3D_SVT_RWSTRUCTURED_BUFFER

The variable is a read-and-write structured buffer.


### -field D3D_SVT_APPEND_STRUCTURED_BUFFER

The variable is an append structured buffer.


### -field D3D_SVT_CONSUME_STRUCTURED_BUFFER

The variable is a consume structured buffer.


### -field D3D_SVT_MIN8FLOAT


            The variable is an 8-byte FLOAT.
          


### -field D3D_SVT_MIN10FLOAT


            The variable is a 10-byte FLOAT.
          


### -field D3D_SVT_MIN16FLOAT


            The variable is a 16-byte FLOAT.
          


### -field D3D_SVT_MIN12INT


            The variable is a 12-byte INT.
          


### -field D3D_SVT_MIN16INT


            The variable is a 16-byte INT.
          


### -field D3D_SVT_MIN16UINT


            The variable is a 16-byte INT.
          


### -field D3D10_SVT_VOID

The variable is a void pointer.


### -field D3D10_SVT_BOOL

The variable is a boolean.


### -field D3D10_SVT_INT

The variable is an integer.


### -field D3D10_SVT_FLOAT

The variable is a floating-point number.


### -field D3D10_SVT_STRING

The variable is a string.


### -field D3D10_SVT_TEXTURE

The variable is a texture.


### -field D3D10_SVT_TEXTURE1D

The variable is a 1D texture.


### -field D3D10_SVT_TEXTURE2D

The variable is a 2D texture.


### -field D3D10_SVT_TEXTURE3D

The variable is a 3D texture.


### -field D3D10_SVT_TEXTURECUBE

The variable is a texture cube.


### -field D3D10_SVT_SAMPLER

The variable is a sampler.


### -field D3D10_SVT_SAMPLER1D


            The variable is a 1D sampler.
          


### -field D3D10_SVT_SAMPLER2D


            The variable is a 2D sampler.
          


### -field D3D10_SVT_SAMPLER3D


            The variable is a 3D sampler.
          


### -field D3D10_SVT_SAMPLERCUBE


            The variable is a cube sampler.
          


### -field D3D10_SVT_PIXELSHADER

The variable is a pixel shader.


### -field D3D10_SVT_VERTEXSHADER

The variable is a vertex shader.


### -field D3D10_SVT_PIXELFRAGMENT


            The variable is a pixel fragment.
          


### -field D3D10_SVT_VERTEXFRAGMENT


            The variable is a vertex fragment.
          


### -field D3D10_SVT_UINT

The variable is an unsigned integer.


### -field D3D10_SVT_UINT8

The variable is an 8-bit unsigned integer.


### -field D3D10_SVT_GEOMETRYSHADER

The variable is a geometry shader.


### -field D3D10_SVT_RASTERIZER

The variable is a rasterizer-state object.


### -field D3D10_SVT_DEPTHSTENCIL

The variable is a depth-stencil-state object.


### -field D3D10_SVT_BLEND

The variable is a blend-state object.


### -field D3D10_SVT_BUFFER

The variable is a buffer.


### -field D3D10_SVT_CBUFFER

The variable is a constant buffer.


### -field D3D10_SVT_TBUFFER

The variable is a texture buffer.


### -field D3D10_SVT_TEXTURE1DARRAY

The variable is a 1D-texture array.


### -field D3D10_SVT_TEXTURE2DARRAY

The variable is a 2D-texture array.


### -field D3D10_SVT_RENDERTARGETVIEW

The variable is a render-target view.


### -field D3D10_SVT_DEPTHSTENCILVIEW

The variable is a depth-stencil view.


### -field D3D10_SVT_TEXTURE2DMS

The variable is a 2D-multisampled texture.


### -field D3D10_SVT_TEXTURE2DMSARRAY

The variable is a 2D-multisampled-texture array.


### -field D3D10_SVT_TEXTURECUBEARRAY

The variable is a texture-cube array.


### -field D3D11_SVT_HULLSHADER

The variable holds a compiled hull-shader binary.


### -field D3D11_SVT_DOMAINSHADER

The variable holds a compiled domain-shader binary.


### -field D3D11_SVT_INTERFACE_POINTER

The variable is an interface.


### -field D3D11_SVT_COMPUTESHADER

The variable holds a compiled compute-shader binary.


### -field D3D11_SVT_DOUBLE

The variable is a double precision (64-bit) floating-point number.


### -field D3D11_SVT_RWTEXTURE1D

The variable is a 1D read-and-write texture.


### -field D3D11_SVT_RWTEXTURE1DARRAY

The variable is an array of 1D read-and-write textures.


### -field D3D11_SVT_RWTEXTURE2D

The variable is a 2D read-and-write texture.


### -field D3D11_SVT_RWTEXTURE2DARRAY

The variable is an array of 2D read-and-write textures.


### -field D3D11_SVT_RWTEXTURE3D

The variable is a 3D read-and-write texture.


### -field D3D11_SVT_RWBUFFER

The variable is a read-and-write buffer.


### -field D3D11_SVT_BYTEADDRESS_BUFFER

The variable is a byte-address buffer.


### -field D3D11_SVT_RWBYTEADDRESS_BUFFER

The variable is a read and write byte-address buffer.


### -field D3D11_SVT_STRUCTURED_BUFFER

The variable is a structured buffer. 


### -field D3D11_SVT_RWSTRUCTURED_BUFFER

The variable is a read-and-write structured buffer.


### -field D3D11_SVT_APPEND_STRUCTURED_BUFFER

The variable is an append structured buffer.


### -field D3D11_SVT_CONSUME_STRUCTURED_BUFFER

The variable is a consume structured buffer.


### -field D3D_SVT_FORCE_DWORD

This value is not used by a programmer; it exists to force the enumeration to compile to 32 bits.


## -remarks




          A call to the
          <a href="https://msdn.microsoft.com/96296270-fcca-4843-bd0a-78c7f87136e5">ID3D11ShaderReflectionType::GetDesc</a>
          method returns a
          <b>D3D_SHADER_VARIABLE_TYPE</b>
          value in the <b>Type</b> member of a
          <a href="https://msdn.microsoft.com/8d2067a3-17f8-4496-a613-581f5e35fe93">D3D11_SHADER_TYPE_DESC</a> structure.
        


          The types in a structured buffer describe the structure of the elements in the buffer.
          The layout of these types generally match their C++ struct counterparts.
          The following examples show structured buffers:
        

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>struct mystruct {float4 val; uint ind;}; RWStructuredBuffer&lt;mystruct&gt; rwbuf;
                                         RWStructuredBuffer&lt;float3&gt; rwbuf2;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

