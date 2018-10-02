---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetRequiresFlags
title: ID3D12ShaderReflection::GetRequiresFlags
author: windows-sdk-content
description: Gets a group of flags that indicates the requirements of a shader.
old-location: direct3d12\id3d12shaderreflection_getrequiresflags.htm
tech.root: direct3d12
ms.assetid: ABA7BB9E-AB1D-407A-BB16-97EE74318C1A
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: GetRequiresFlags, GetRequiresFlags method, GetRequiresFlags method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetRequiresFlags method, ID3D12ShaderReflection.GetRequiresFlags, ID3D12ShaderReflection::GetRequiresFlags, d3d12shader/ID3D12ShaderReflection::GetRequiresFlags, direct3d12.id3d12shaderreflection_getrequiresflags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d12shader.h
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
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12ShaderReflection.GetRequiresFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12ShaderReflection::GetRequiresFlags


## -description


Gets a group of flags that indicates the requirements of a shader.
        


## -parameters






## -returns



Type: <b>UINT64</b>

A value that contains a combination of one or more shader requirements #define flags; each flag specifies a requirement of the shader.
              A default value of 0 means there are no requirements.
            

<table>
<tr>
<th>Shader requirement #define flag</th>
<th>Description</th>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_DOUBLES</b></td>
<td>Shader requires that the graphics driver and hardware support double data type.
                  </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_EARLY_DEPTH_STENCIL</b></td>
<td>Shader requires an early depth stencil.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_UAVS_AT_EVERY_STAGE</b></td>
<td>Shader requires unordered access views (UAVs) at every pipeline stage.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_64_UAVS</b></td>
<td>Shader requires 64 UAVs.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_MINIMUM_PRECISION</b></td>
<td>Shader requires the graphics driver and hardware to support minimum precision.
                  For more info, see <a href="https://msdn.microsoft.com/en-us/library/Hh968108(v=VS.85).aspx">Using HLSL minimum precision</a>.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_11_1_DOUBLE_EXTENSIONS</b></td>
<td>Shader requires that the graphics driver and hardware support extended doubles instructions.
                  For more info, see the <b>ExtendedDoublesShaderInstructions</b> member of <a href="https://msdn.microsoft.com/en-us/library/Dn770364(v=VS.85).aspx">D3D12_FEATURE_DATA_D3D12_OPTIONS</a>.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_11_1_SHADER_EXTENSIONS</b></td>
<td>Shader requires that the graphics driver and hardware support the <a href="https://msdn.microsoft.com/en-us/library/Hh768927(v=VS.85).aspx">msad4</a> intrinsic function in shaders.
                  For more info, see the <b>SAD4ShaderInstructions</b> member of <a href="https://msdn.microsoft.com/en-us/library/Dn770364(v=VS.85).aspx">D3D12_FEATURE_DATA_D3D12_OPTIONS</a>.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_LEVEL_9_COMPARISON_FILTERING</b></td>
<td>Shader requires that the graphics driver and hardware support Direct3D 9 shadow support.
                  </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_TILED_RESOURCES</b></td>
<td>Shader requires that the graphics driver and hardware support tiled resources.
                  </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_STENCIL_REF</b></td>
<td>Shader requires a reference value for depth stencil tests.
                  For more info, see the <b>PSSpecifiedStencilRefSupported</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Dn770364(v=VS.85).aspx">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure,
                  and <a href="https://msdn.microsoft.com/en-us/library/Dn903887(v=VS.85).aspx">ID3D12GraphicsCommandList::OMSetStencilRef</a>.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_INNER_COVERAGE</b></td>
<td>Shader requires that the graphics driver and hardware support inner coverage.For more info, see the enumeration constants D3D_NAME_INNER_COVERAGE and D3D11_NAME_INNER_COVERAGE in <a href="https://msdn.microsoft.com/en-us/library/Ff728724(v=VS.85).aspx">D3D_NAME</a>.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_TYPED_UAV_LOAD_ADDITIONAL_FORMATS</b></td>
<td>Shader requires that the graphics driver and hardware support the loading of additional formats for typed unordered-access views (UAVs).
                  See the <b>TypedUAVLoadAdditionalFormats</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Dn770364(v=VS.85).aspx">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_ROVS</b></td>
<td>Shader requires that the graphics driver and hardware support rasterizer ordered views (ROVs).
                  See <a href="https://msdn.microsoft.com/D308BF3E-8CBE-4DF0-B020-4D202E858D99">Rasterizer Ordered Views</a>.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_VIEWPORT_AND_RT_ARRAY_INDEX_FROM_ANY_SHADER_FEEDING_RASTERIZER</b></td>
<td>Shader requires that the graphics driver and hardware support viewport and render target array index values from any shader-feeding rasterizer.For more info, see the member <b>VPAndRTArrayIndexFromAnyShaderFeedingRasterizerSupportedWithoutGSEmulation</b>of the <a href="https://msdn.microsoft.com/en-us/library/Dn770364(v=VS.85).aspx">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure.
                </td>
</tr>
</table>
 




## -remarks



Here is how the D3D12Shader.h header defines the shader requirements flags:
        


```cpp
#define D3D_SHADER_REQUIRES_DOUBLES                                                         0x00000001
#define D3D_SHADER_REQUIRES_EARLY_DEPTH_STENCIL                                             0x00000002
#define D3D_SHADER_REQUIRES_UAVS_AT_EVERY_STAGE                                             0x00000004
#define D3D_SHADER_REQUIRES_64_UAVS                                                         0x00000008
#define D3D_SHADER_REQUIRES_MINIMUM_PRECISION                                               0x00000010
#define D3D_SHADER_REQUIRES_11_1_DOUBLE_EXTENSIONS                                          0x00000020
#define D3D_SHADER_REQUIRES_11_1_SHADER_EXTENSIONS                                          0x00000040
#define D3D_SHADER_REQUIRES_LEVEL_9_COMPARISON_FILTERING                                    0x00000080
#define D3D_SHADER_REQUIRES_TILED_RESOURCES                                                 0x00000100
#define D3D_SHADER_REQUIRES_STENCIL_REF                                                     0x00000200
#define D3D_SHADER_REQUIRES_INNER_COVERAGE                                                  0x00000400
#define D3D_SHADER_REQUIRES_TYPED_UAV_LOAD_ADDITIONAL_FORMATS                               0x00000800
#define D3D_SHADER_REQUIRES_ROVS                                                            0x00001000
#define D3D_SHADER_REQUIRES_VIEWPORT_AND_RT_ARRAY_INDEX_FROM_ANY_SHADER_FEEDING_RASTERIZER  0x00002000

```





## -see-also




<a href="https://msdn.microsoft.com/0C40C73E-06F3-41FA-AA27-2C0B730B357B">Checking Hardware Feature Support</a>



<a href="https://msdn.microsoft.com/145F2CCB-C076-42BE-8AF4-74349CDF6B02">ID3D12ShaderReflection</a>
 

 

