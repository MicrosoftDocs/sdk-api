---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetRequiresFlags
title: ID3D12ShaderReflection::GetRequiresFlags (d3d12shader.h)
description: Gets a group of flags that indicates the requirements of a shader. (ID3D12ShaderReflection.GetRequiresFlags)
helpviewer_keywords: ["GetRequiresFlags","GetRequiresFlags method","GetRequiresFlags method","ID3D12ShaderReflection interface","ID3D12ShaderReflection interface","GetRequiresFlags method","ID3D12ShaderReflection.GetRequiresFlags","ID3D12ShaderReflection::GetRequiresFlags","d3d12shader/ID3D12ShaderReflection::GetRequiresFlags","direct3d12.id3d12shaderreflection_getrequiresflags"]
old-location: direct3d12\id3d12shaderreflection_getrequiresflags.htm
tech.root: direct3d12
ms.assetid: ABA7BB9E-AB1D-407A-BB16-97EE74318C1A
ms.date: 12/05/2018
ms.keywords: GetRequiresFlags, GetRequiresFlags method, GetRequiresFlags method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetRequiresFlags method, ID3D12ShaderReflection.GetRequiresFlags, ID3D12ShaderReflection::GetRequiresFlags, d3d12shader/ID3D12ShaderReflection::GetRequiresFlags, direct3d12.id3d12shaderreflection_getrequiresflags
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12ShaderReflection::GetRequiresFlags
 - d3d12shader/ID3D12ShaderReflection::GetRequiresFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12ShaderReflection.GetRequiresFlags
---

# ID3D12ShaderReflection::GetRequiresFlags


## -description

Gets a group of flags that indicates the requirements of a shader.



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
                  For more info, see <a href="/windows/desktop/direct3dhlsl/using-hlsl-minimum-precision">Using HLSL minimum precision</a>.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_11_1_DOUBLE_EXTENSIONS</b></td>
<td>Shader requires that the graphics driver and hardware support extended doubles instructions.
                  For more info, see the <b>ExtendedDoublesShaderInstructions</b> member of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a>.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_11_1_SHADER_EXTENSIONS</b></td>
<td>Shader requires that the graphics driver and hardware support the <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-msad4">msad4</a> intrinsic function in shaders.
                  For more info, see the <b>SAD4ShaderInstructions</b> member of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a>.
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
                  For more info, see the <b>PSSpecifiedStencilRefSupported</b> member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure,
                  and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref">ID3D12GraphicsCommandList::OMSetStencilRef</a>.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_INNER_COVERAGE</b></td>
<td>Shader requires that the graphics driver and hardware support inner coverage.For more info, see the enumeration constants D3D_NAME_INNER_COVERAGE and D3D11_NAME_INNER_COVERAGE in <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_name">D3D_NAME</a>.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_TYPED_UAV_LOAD_ADDITIONAL_FORMATS</b></td>
<td>Shader requires that the graphics driver and hardware support the loading of additional formats for typed unordered-access views (UAVs).
                  See the <b>TypedUAVLoadAdditionalFormats</b> member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_ROVS</b></td>
<td>Shader requires that the graphics driver and hardware support rasterizer ordered views (ROVs).
                  See <a href="/windows/desktop/direct3d12/rasterizer-order-views">Rasterizer Ordered Views</a>.
                </td>
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_VIEWPORT_AND_RT_ARRAY_INDEX_FROM_ANY_SHADER_FEEDING_RASTERIZER</b></td>
<td>Shader requires that the graphics driver and hardware support viewport and render target array index values from any shader-feeding rasterizer.For more info, see the member <b>VPAndRTArrayIndexFromAnyShaderFeedingRasterizerSupportedWithoutGSEmulation</b> of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure.
                </td>
</tr>
 
</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_WAVE_OPS</b></td>
<td>Shader requires that the graphics driver and hardware support wave ops. For more info, see the member <b>WaveOps</b> of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1">D3D12_FEATURE_DATA_D3D12_OPTIONS1</a> structure.</td>
</tr>

</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_INT64_OPS</b></td>
<td>Shader requires that the graphics driver and hardware support 64-bit integer ops. For more info, see the member <b>Int64ShaderOps</b> of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1">D3D12_FEATURE_DATA_D3D12_OPTIONS1</a> structure.</td>
</tr>

</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_VIEW_ID</b></td>
<td>Shader requires that the graphics driver and hardware support view instancing using <b>SV_ViewID</b>. For more info, see the member <b>ViewInstancingTier</b> of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3">D3D12_FEATURE_DATA_D3D12_OPTIONS3</a> structure.</td>
</tr>

</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_BARYCENTRICS</b></td>
<td>Shader requires that the graphics driver and hardware support barycentrics using <b>SV_Barycentrics</b>. For more info, see the member <b>BarycentricsSupported</b> of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3">D3D12_FEATURE_DATA_D3D12_OPTIONS3</a> structure.</td>
</tr>

</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_NATIVE_16BIT_OPS</b></td>
<td>Shader requires that the graphics driver and hardware support native 16-bit ops. For more info, see the member <b>Native16BitShaderOpsSupported</b> of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4">D3D12_FEATURE_DATA_D3D12_OPTIONS4</a> structure.</td>
</tr>

</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_SHADING_RATE</b></td>
<td>Shader requires that the graphics driver and hardware support the Variable Shading Rate (VRS) feature. For more info, see the member <b>VariableShadingRateTier</b> of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6">D3D12_FEATURE_DATA_D3D12_OPTIONS6</a> structure.</td>
</tr>

</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_RAYTRACING_TIER_1_1</b></td>
<td>Shader requires that the graphics driver and hardware support DXR tier 1.1. For more info, see the member <b>RaytracingTier</b> of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5">D3D12_FEATURE_DATA_D3D12_OPTIONS5</a> structure.</td>
</tr>

</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_SAMPLER_FEEDBACK</b></td>
<td>Shader requires that the graphics driver and hardware support Sampler Feedback. For more info, see the member <b>SamplerFeedbackTier</b> of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options7">D3D12_FEATURE_DATA_D3D12_OPTIONS7</a> structure.</td>
</tr>

</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_ATOMIC_INT64_ON_TYPED_RESOURCE</b></td>
<td>Shader requires that the graphics driver and hardware support int64 atomics on typed resources. For more info, see the member <b>AtomicInt64OnTypedResourceSupported</b> of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options9">D3D12_FEATURE_DATA_D3D12_OPTIONS9</a> structure.</td>
</tr>

</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_ATOMIC_INT64_ON_GROUP_SHARED</b></td>
<td>Shader requires that the graphics driver and hardware support int64 atomics on groupshared memory. For more info, see the member <b>AtomicInt64OnGroupSharedSupported</b> of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options9">D3D12_FEATURE_DATA_D3D12_OPTIONS9</a> structure.</td>
</tr>

</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_DERIVATIVES_IN_MESH_AND_AMPLIFICATION_SHADERS</b></td>
<td>Shader requires that the graphics driver and hardware support derivatives in mesh and amplification shaders. For more info, see the member <b>DerivativesInMeshAndAmplificationShadersSupported</b> of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options9">D3D12_FEATURE_DATA_D3D12_OPTIONS9</a> structure.</td>
</tr>

</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_RESOURCE_DESCRIPTOR_HEAP_INDEXING</b></td>
<td>Shader requires that the graphics driver and hardware support Dynamic Resources (a requirement for Shader Model 6.6) and the <b>ResourceDescriptorHeap</b> in particular. For more info, see the <a href="/DirectX-Specs/d3d/HLSL_SM_6_6_DynamicResources.html">HLSL Dynamic Resources</a> spec document.</td>
</tr>

</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_SAMPLER_DESCRIPTOR_HEAP_INDEXING</b></td>
<td>Shader requires that the graphics driver and hardware support Dynamic Resources (a requirement for Shader Model 6.6) and the <b>SamplerDescriptorHeap</b> in particular. For more info, see the <a href="/DirectX-Specs/d3d/HLSL_SM_6_6_DynamicResources.html">HLSL Dynamic Resources</a> spec document.</td>
</tr>

</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_WAVE_MMA</b></td>
<td>Shader requires that the graphics driver and hardware support Wave MMA. For more info, see the member <b>WaveMMATier</b> of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options9">D3D12_FEATURE_DATA_D3D12_OPTIONS9</a> structure.</td>
</tr>

</tr>
<tr>
<td><b>D3D_SHADER_REQUIRES_ATOMIC_INT64_ON_DESCRIPTOR_HEAP_RESOURCE</b></td>
<td>Shader requires that the graphics driver and hardware support int64 atomics on descriptor heap resources. For more info, see the member <b>AtomicInt64OnDescriptorHeapResourceSupported</b> of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options11">D3D12_FEATURE_DATA_D3D12_OPTIONS11</a> structure.</td>
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
#define D3D_SHADER_REQUIRES_WAVE_OPS                                                        0x00004000
#define D3D_SHADER_REQUIRES_INT64_OPS                                                       0x00008000
#define D3D_SHADER_REQUIRES_VIEW_ID                                                         0x00010000
#define D3D_SHADER_REQUIRES_BARYCENTRICS                                                    0x00020000
#define D3D_SHADER_REQUIRES_NATIVE_16BIT_OPS                                                0x00040000
#define D3D_SHADER_REQUIRES_SHADING_RATE                                                    0x00080000
#define D3D_SHADER_REQUIRES_RAYTRACING_TIER_1_1                                             0x00100000
#define D3D_SHADER_REQUIRES_SAMPLER_FEEDBACK                                                0x00200000
#define D3D_SHADER_REQUIRES_ATOMIC_INT64_ON_TYPED_RESOURCE                                  0x00400000
#define D3D_SHADER_REQUIRES_ATOMIC_INT64_ON_GROUP_SHARED                                    0x00800000
#define D3D_SHADER_REQUIRES_DERIVATIVES_IN_MESH_AND_AMPLIFICATION_SHADERS                   0x01000000
#define D3D_SHADER_REQUIRES_RESOURCE_DESCRIPTOR_HEAP_INDEXING                               0x02000000
#define D3D_SHADER_REQUIRES_SAMPLER_DESCRIPTOR_HEAP_INDEXING                                0x04000000
#define D3D_SHADER_REQUIRES_WAVE_MMA                                                        0x08000000
#define D3D_SHADER_REQUIRES_ATOMIC_INT64_ON_DESCRIPTOR_HEAP_RESOURCE                        0x10000000
```

## -see-also

<a href="/windows/desktop/direct3ddxgi/checking-hardware-feature-support">Checking Hardware Feature Support</a>



<a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection">ID3D12ShaderReflection</a>
