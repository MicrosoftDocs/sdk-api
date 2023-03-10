---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetRequiresFlags
title: ID3D11ShaderReflection::GetRequiresFlags (d3d11shader.h)
description: Gets a group of flags that indicates the requirements of a shader. (ID3D11ShaderReflection.GetRequiresFlags)
helpviewer_keywords: ["GetRequiresFlags","GetRequiresFlags method [Direct3D 11]","GetRequiresFlags method [Direct3D 11]","ID3D11ShaderReflection interface","ID3D11ShaderReflection interface [Direct3D 11]","GetRequiresFlags method","ID3D11ShaderReflection.GetRequiresFlags","ID3D11ShaderReflection::GetRequiresFlags","d3d11shader/ID3D11ShaderReflection::GetRequiresFlags","direct3d11.id3d11shaderreflection_getrequiresflags"]
old-location: direct3d11\id3d11shaderreflection_getrequiresflags.htm
tech.root: direct3d11
ms.assetid: BC70E68A-8909-42F9-9AEE-017BA682D635
ms.date: 12/05/2018
ms.keywords: GetRequiresFlags, GetRequiresFlags method [Direct3D 11], GetRequiresFlags method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetRequiresFlags method, ID3D11ShaderReflection.GetRequiresFlags, ID3D11ShaderReflection::GetRequiresFlags, d3d11shader/ID3D11ShaderReflection::GetRequiresFlags, direct3d11.id3d11shaderreflection_getrequiresflags
req.header: d3d11shader.h
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
req.lib: D3DCompiler_47.lib
req.dll: D3DCompiler_47.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11ShaderReflection::GetRequiresFlags
 - d3d11shader/ID3D11ShaderReflection::GetRequiresFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11ShaderReflection.GetRequiresFlags
---

# ID3D11ShaderReflection::GetRequiresFlags


## -description

Gets a group of flags that indicates the requirements of a shader.



## -returns

Type: <b>UINT64</b>

A value that contains a combination of one or more shader requirements flags; each flag specifies a requirement of the shader. A default value of 0 means there are no requirements. 

<table>
<tr>
<th>Shader requirement flag</th>
<th>Description</th>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_DOUBLES</b></td>
<td>Shader requires that the graphics driver and hardware support double data type. For more info, see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_doubles">D3D11_FEATURE_DATA_DOUBLES</a>.</td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_EARLY_DEPTH_STENCIL</b></td>
<td>Shader requires an early depth stencil.</td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_UAVS_AT_EVERY_STAGE</b></td>
<td>Shader requires unordered access views (UAVs) at every pipeline stage.</td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_64_UAVS</b></td>
<td>Shader requires 64 UAVs.</td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_MINIMUM_PRECISION</b></td>
<td>Shader requires the graphics driver and hardware to support minimum precision. For more info, see <a href="/windows/desktop/direct3dhlsl/using-hlsl-minimum-precision">Using HLSL minimum precision</a>.</td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_11_1_DOUBLE_EXTENSIONS</b></td>
<td>Shader requires that the graphics driver and hardware support extended doubles instructions. For more info, see the <b>ExtendedDoublesShaderInstructions</b> member of <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options">D3D11_FEATURE_DATA_D3D11_OPTIONS</a>.</td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_11_1_SHADER_EXTENSIONS</b></td>
<td>Shader requires that the graphics driver and hardware support the <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-msad4">msad4</a> intrinsic function in shaders. For more info, see the <b>SAD4ShaderInstructions</b> member of <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options">D3D11_FEATURE_DATA_D3D11_OPTIONS</a>.</td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_LEVEL_9_COMPARISON_FILTERING</b></td>
<td>Shader requires that the graphics driver and hardware support Direct3D 9 shadow support. For more info, see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support">D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</a>.</td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_TILED_RESOURCES</b></td>
<td>Shader requires that the graphics driver and hardware support tiled resources. For more info, see <a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11device2-getresourcetiling">GetResourceTiling</a>. </td>
</tr>
</table>

## -remarks

Here is how the D3D11Shader.h header defines the shader requirements flags:


```cpp

#define D3D_SHADER_REQUIRES_DOUBLES                         0x00000001
#define D3D_SHADER_REQUIRES_EARLY_DEPTH_STENCIL             0x00000002
#define D3D_SHADER_REQUIRES_UAVS_AT_EVERY_STAGE             0x00000004
#define D3D_SHADER_REQUIRES_64_UAVS                         0x00000008
#define D3D_SHADER_REQUIRES_MINIMUM_PRECISION               0x00000010
#define D3D_SHADER_REQUIRES_11_1_DOUBLE_EXTENSIONS          0x00000020
#define D3D_SHADER_REQUIRES_11_1_SHADER_EXTENSIONS          0x00000040
#define D3D_SHADER_REQUIRES_LEVEL_9_COMPARISON_FILTERING    0x00000080

```

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection">ID3D11ShaderReflection</a>
