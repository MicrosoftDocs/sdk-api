---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetRequiresFlags
title: ID3D12ShaderReflection::GetRequiresFlags (d3d12shader.h)
description: Gets a group of flags that indicates the requirements of a shader. (ID3D12ShaderReflection.GetRequiresFlags)
helpviewer_keywords: ["GetRequiresFlags","GetRequiresFlags method","GetRequiresFlags method","ID3D12ShaderReflection interface","ID3D12ShaderReflection interface","GetRequiresFlags method","ID3D12ShaderReflection.GetRequiresFlags","ID3D12ShaderReflection::GetRequiresFlags","d3d12shader/ID3D12ShaderReflection::GetRequiresFlags","direct3d12.id3d12shaderreflection_getrequiresflags"]
old-location: direct3d12\id3d12shaderreflection_getrequiresflags.htm
tech.root: direct3d12
ms.assetid: ABA7BB9E-AB1D-407A-BB16-97EE74318C1A
ms.date: 06/09/2023
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

## -description

Retrieves a group of flags that indicate the requirements of a shader.

## -returns

Type: **UINT64**

A value that contains a combination of one or more shader requirements `#define` flags; each flag specifies a requirement of the shader. A default value of 0 means that there are no requirements.

**D3D_SHADER_REQUIRES_DOUBLES**. Shader requires that the graphics driver and hardware support the *double* data type.

**D3D_SHADER_REQUIRES_EARLY_DEPTH_STENCIL**. Shader requires an early depth stencil.

**D3D_SHADER_REQUIRES_UAVS_AT_EVERY_STAGE**. Shader requires unordered access views (UAVs) at every pipeline stage.

**D3D_SHADER_REQUIRES_64_UAVS**. Shader requires 64 UAVs.

**D3D_SHADER_REQUIRES_MINIMUM_PRECISION**. Shader requires the graphics driver and hardware to support minimum precision. For more info, see [Using HLSL minimum precision](/windows/win32/direct3dhlsl/using-hlsl-minimum-precision).

**D3D_SHADER_REQUIRES_11_1_DOUBLE_EXTENSIONS**. Shader requires that the graphics driver and hardware support extended doubles instructions. For more info, see the **ExtendedDoublesShaderInstructions** member of [D3D12_FEATURE_DATA_D3D12_OPTIONS](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).

**D3D_SHADER_REQUIRES_11_1_SHADER_EXTENSIONS**. Shader requires that the graphics driver and hardware support the [msad4](/windows/win32/direct3dhlsl/dx-graphics-hlsl-msad4) intrinsic function in shaders. For more info, see the **SAD4ShaderInstructions** member of [D3D12_FEATURE_DATA_D3D12_OPTIONS](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).

**D3D_SHADER_REQUIRES_LEVEL_9_COMPARISON_FILTERING**. Shader requires that the graphics driver and hardware support Direct3D 9 shadow support.

**D3D_SHADER_REQUIRES_TILED_RESOURCES**. Shader requires that the graphics driver and hardware support tiled resources.

**D3D_SHADER_REQUIRES_STENCIL_REF**. Shader requires a reference value for depth stencil tests. For more info, see the **PSSpecifiedStencilRefSupported** member of the [D3D12_FEATURE_DATA_D3D12_OPTIONS](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) structure, and [ID3D12GraphicsCommandList::OMSetStencilRef](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref).

**D3D_SHADER_REQUIRES_INNER_COVERAGE**. Shader requires that the graphics driver and hardware support inner coverage. For more info, see the enumeration constants **D3D_NAME_INNER_COVERAGE** and **D3D11_NAME_INNER_COVERAGE** in [D3D_NAME](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_name).

**D3D_SHADER_REQUIRES_TYPED_UAV_LOAD_ADDITIONAL_FORMATS**. Shader requires that the graphics driver and hardware support the loading of additional formats for typed unordered-access views (UAVs). See the *TypedUAVLoadAdditionalFormats* member of the [D3D12_FEATURE_DATA_D3D12_OPTIONS](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) structure.

**D3D_SHADER_REQUIRES_ROVS**. Shader requires that the graphics driver and hardware support rasterizer ordered views (ROVs). See [Rasterizer Ordered Views](/windows/win32/direct3d12/rasterizer-order-views).

**D3D_SHADER_REQUIRES_VIEWPORT_AND_RT_ARRAY_INDEX_FROM_ANY_SHADER_FEEDING_RASTERIZER**. 
Shader requires that the graphics driver and hardware support viewport and render target array index values from any shader-feeding rasterizer. For more info, see the member *VPAndRTArrayIndexFromAnyShaderFeedingRasterizerSupportedWithoutGSEmulation* of the [D3D12_FEATURE_DATA_D3D12_OPTIONS](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) structure.

**D3D_SHADER_REQUIRES_WAVE_OPS**. Shader requires that the graphics driver and hardware support wave ops. For more info, see the member **WaveOps** of the [D3D12_FEATURE_DATA_D3D12_OPTIONS1](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1) structure.

**D3D_SHADER_REQUIRES_INT64_OPS**. Shader requires that the graphics driver and hardware support 64-bit integer ops. For more info, see the member **Int64ShaderOps** of the [D3D12_FEATURE_DATA_D3D12_OPTIONS1](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1) structure.

**D3D_SHADER_REQUIRES_VIEW_ID**. Shader requires that the graphics driver and hardware support view instancing using **SV_ViewID**. For more info, see the member **ViewInstancingTier** of the [D3D12_FEATURE_DATA_D3D12_OPTIONS3](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) structure.

**D3D_SHADER_REQUIRES_BARYCENTRICS**. Shader requires that the graphics driver and hardware support barycentrics using **SV_Barycentrics**. For more info, see the member **BarycentricsSupported** of the [D3D12_FEATURE_DATA_D3D12_OPTIONS3](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) structure.

**D3D_SHADER_REQUIRES_NATIVE_16BIT_OPS**. Shader requires that the graphics driver and hardware support native 16-bit ops. For more info, see the member **Native16BitShaderOpsSupported** of the [D3D12_FEATURE_DATA_D3D12_OPTIONS4](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4) structure.

**D3D_SHADER_REQUIRES_SHADING_RATE**. Shader requires that the graphics driver and hardware support the Variable Shading Rate (VRS) feature. For more info, see the member **VariableShadingRateTier** of the [D3D12_FEATURE_DATA_D3D12_OPTIONS6](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) structure.

**D3D_SHADER_REQUIRES_RAYTRACING_TIER_1_1**. Shader requires that the graphics driver and hardware support DXR tier 1.1. For more info, see the member **RaytracingTier** of the [D3D12_FEATURE_DATA_D3D12_OPTIONS5](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5) structure.

**D3D_SHADER_REQUIRES_SAMPLER_FEEDBACK**. Shader requires that the graphics driver and hardware support Sampler Feedback. For more info, see the member **SamplerFeedbackTier** of the [D3D12_FEATURE_DATA_D3D12_OPTIONS7](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options7) structure.

**D3D_SHADER_REQUIRES_ATOMIC_INT64_ON_TYPED_RESOURCE**. Shader requires that the graphics driver and hardware support int64 atomics on typed resources. For more info, see the member **AtomicInt64OnTypedResourceSupported** of the [D3D12_FEATURE_DATA_D3D12_OPTIONS9](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options9) structure.

**D3D_SHADER_REQUIRES_ATOMIC_INT64_ON_GROUP_SHARED**. Shader requires that the graphics driver and hardware support int64 atomics on groupshared memory. For more info, see the member **AtomicInt64OnGroupSharedSupported** of the [D3D12_FEATURE_DATA_D3D12_OPTIONS9](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options9) structure.

**D3D_SHADER_REQUIRES_DERIVATIVES_IN_MESH_AND_AMPLIFICATION_SHADERS**. Shader requires that the graphics driver and hardware support derivatives in mesh and amplification shaders. For more info, see the member **DerivativesInMeshAndAmplificationShadersSupported** of the [D3D12_FEATURE_DATA_D3D12_OPTIONS9](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options9) structure.

**D3D_SHADER_REQUIRES_RESOURCE_DESCRIPTOR_HEAP_INDEXING**. Shader requires that the graphics driver and hardware support Dynamic Resources (a requirement for Shader Model 6.6) and the **ResourceDescriptorHeap** in particular. For more info, see the [HLSL dynamic resources](https://github.com/microsoft/DirectX-Specs/blob/master/d3d/HLSL_SM_6_6_DynamicResources.md) spec on GitHub.

**D3D_SHADER_REQUIRES_SAMPLER_DESCRIPTOR_HEAP_INDEXING**. Shader requires that the graphics driver and hardware support Dynamic Resources (a requirement for Shader Model 6.6) and the **SamplerDescriptorHeap** in particular. For more info, see the [HLSL dynamic resources](https://github.com/microsoft/DirectX-Specs/blob/master/d3d/HLSL_SM_6_6_DynamicResources.md) spec on GitHub.

**D3D_SHADER_REQUIRES_WAVE_MMA**. Shader requires that the graphics driver and hardware support Wave MMA. For more info, see the member **WaveMMATier** of the [D3D12_FEATURE_DATA_D3D12_OPTIONS9](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options9) structure.

**D3D_SHADER_REQUIRES_ATOMIC_INT64_ON_DESCRIPTOR_HEAP_RESOURCE**. Shader requires that the graphics driver and hardware support int64 atomics on descriptor heap resources. For more info, see the member **AtomicInt64OnDescriptorHeapResourceSupported** of the [D3D12_FEATURE_DATA_D3D12_OPTIONS11](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options11) structure.

## -remarks

Here's how the `d3d12shader.h` header file defines the shader requirements flags:

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

* [Checking hardware feature support](/windows/win32/direct3ddxgi/checking-hardware-feature-support)
* [ID3D12ShaderReflection](/windows/win32/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection)
