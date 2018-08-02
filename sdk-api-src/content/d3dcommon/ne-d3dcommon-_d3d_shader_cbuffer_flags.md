---
UID: NE:d3dcommon._D3D_SHADER_CBUFFER_FLAGS
title: "_D3D_SHADER_CBUFFER_FLAGS"
author: windows-sdk-content
description: These flags identify constant-buffer properties.
old-location: direct3d10\d3d10_shader_cbuffer_flags.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_cbuffer_flags.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 440464c2-f4d0-b8bc-8a22-baf84dd2acd0, D3D10_CBF_FORCE_DWORD, D3D10_CBF_USERPACKED, D3D10_SHADER_CBUFFER_FLAGS, D3D10_SHADER_CBUFFER_FLAGS enumeration [Direct3D 10], D3D_SHADER_CBUFFER_FLAGS, LPD3D10_SHADER_CBUFFER_FLAGS, LPD3D10_SHADER_CBUFFER_FLAGS enumeration pointer [Direct3D 10], _D3D_SHADER_CBUFFER_FLAGS, d3d10shader/D3D10_CBF_FORCE_DWORD, d3d10shader/D3D10_CBF_USERPACKED, d3d10shader/D3D10_SHADER_CBUFFER_FLAGS, d3d10shader/LPD3D10_SHADER_CBUFFER_FLAGS, d3dcommon/D3D10_CBF_FORCE_DWORD, d3dcommon/D3D10_CBF_USERPACKED, d3dcommon/D3D10_SHADER_CBUFFER_FLAGS, d3dcommon/LPD3D10_SHADER_CBUFFER_FLAGS, direct3d10.d3d10_shader_cbuffer_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3dcommon.h
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
tech.root: 
req.typenames: D3D_SHADER_CBUFFER_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10Shader.h
 - d3dcommon.h
api_name:
 - D3D10_SHADER_CBUFFER_FLAGS
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# _D3D_SHADER_CBUFFER_FLAGS enumeration


## -description


These flags identify constant-buffer properties.


## -enum-fields




### -field D3D_CBF_USERPACKED


### -field D3D10_CBF_USERPACKED

Bind the constant buffer to an input slot defined in HLSL code (instead of letting the compiler choose the input slot).


### -field D3D_CBF_FORCE_DWORD




#### - D3D10_CBF_FORCE_DWORD

This value is not used by a programmer; it exists to force the enumeration to compile to 32 bits.


## -remarks



These flags are used in a shader buffer description (see <a href="https://msdn.microsoft.com/en-us/library/Bb172417(v=VS.85).aspx">D3D10_SHADER_BUFFER_DESC</a>).

The    <b>D3D10_SHADER_CBUFFER_FLAGS</b> enumeration is type defined in the  D3D10shader.h header file as a <a href="https://msdn.microsoft.com/f641b3ec-5492-4835-9cf6-e41447e4b6b6">D3D_SHADER_CBUFFER_FLAGS</a> enumeration, which is fully defined in the  D3DCommon.h header file.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef D3D_SHADER_CBUFFER_FLAGS D3D10_SHADER_CBUFFER_FLAGS;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205156(v=VS.85).aspx">Shader Enumerations</a>
 

 

