---
UID: NS:d3dcompiler._D3D_SHADER_DATA
title: D3D_SHADER_DATA (d3dcompiler.h)
author: windows-sdk-content
description: Describes shader data.
old-location: direct3dhlsl\d3d_shader_data.htm
tech.root: direct3dhlsl
ms.assetid: 34cde0c9-e8ee-428d-86f5-87c91b95f5d8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D_SHADER_DATA, D3D_SHADER_DATA structure [HLSL], _D3D_SHADER_DATA, d3dcompiler/D3D_SHADER_DATA, direct3dhlsl.d3d_shader_data
ms.topic: struct
req.header: d3dcompiler.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3Dcompiler.h
api_name:
 - D3D_SHADER_DATA
product: Windows
targetos: Windows
req.typenames: D3D_SHADER_DATA
req.redist: 
ms.custom: 19H1
---

# D3D_SHADER_DATA structure


## -description


Describes shader data.


## -struct-fields




### -field pBytecode

A pointer to shader data.


### -field BytecodeLength

Length of shader data that <b>pBytecode</b> points to.


## -remarks



An array of <b>D3D_SHADER_DATA</b> structures is passed to <a href="https://msdn.microsoft.com/e53a0d36-3cd4-4327-8969-6a864b38a15b">D3DCompressShaders</a> to compress the shader data into a more compact form.




## -see-also




<a href="https://msdn.microsoft.com/1439305e-5620-40f9-a6cb-17eed6689b29">Structures</a>
 

 

