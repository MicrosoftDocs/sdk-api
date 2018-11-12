---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS
title: D3D12_FEATURE_DATA_D3D12_OPTIONS
author: windows-sdk-content
description: Describes Direct3D 12 feature options in the current graphics driver.
old-location: direct3d12\d3d12_feature_data_d3d12_options.htm
tech.root: direct3d12
ms.assetid: 3193E3CC-C6CA-43D4-8D8C-41B7FCEE2BDF
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: D3D12_FEATURE_DATA_D3D12_OPTIONS, D3D12_FEATURE_DATA_D3D12_OPTIONS structure, d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS, direct3d12.d3d12_feature_data_d3d12_options
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d12.h
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
 - D3D12.h
api_name:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS
product: Windows
targetos: Windows
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS
req.redist: 
---

# D3D12_FEATURE_DATA_D3D12_OPTIONS structure


## -description


Describes Direct3D 12 feature options in the current graphics driver.
        


## -struct-fields




### -field DoublePrecisionFloatShaderOps

Specifies whether <b>double</b> types are allowed for shader operations.
              If <b>TRUE</b>, double types are allowed; otherwise <b>FALSE</b>.
              The supported operations are equivalent to Direct3D 11's <b>ExtendedDoublesShaderInstructions</b> member of the <a href="https://msdn.microsoft.com/02A3B423-75AB-4F44-BEBE-B8039EF384DC">D3D11_FEATURE_DATA_D3D11_OPTIONS</a> structure.
            

To use any HLSL shader that is compiled with a <b>double</b> type,
              the runtime must set <b>DoublePrecisionFloatShaderOps</b> to <b>TRUE</b>.
            


### -field OutputMergerLogicOp

Specifies whether logic operations are available in blend state. The runtime sets this member to <b>TRUE</b> if logic operations are available in blend state and <b>FALSE</b> otherwise. This member is <b>FALSE</b> for feature level 9.1, 9.2, and 9.3.  This member is optional for feature level 10, 10.1, and 11.  This member is <b>TRUE</b> for feature level 11.1 and 12.
          


### -field MinPrecisionSupport

A combination of <a href="https://msdn.microsoft.com/04172EA4-B663-49B4-A329-E4B0A8EE4617">D3D12_SHADER_MIN_PRECISION_SUPPORT</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies minimum precision levels that the driver supports for shader stages. A value of zero indicates that the driver supports only full 32-bit precision for all shader stages.
          


### -field TiledResourcesTier

Specifies whether the hardware and driver support tiled resources. The runtime sets this member to a <a href="https://msdn.microsoft.com/ADBA96C3-BD9E-4F12-89C8-371F6F7D369D">D3D12_TILED_RESOURCES_TIER</a>-typed value that indicates if the hardware and driver support tiled resources and at what tier level.
          


### -field ResourceBindingTier

Specifies the level at which the hardware and driver support resource binding. The runtime sets this member to a <a href="https://msdn.microsoft.com/en-us/library/Dn770394(v=VS.85).aspx">D3D12_RESOURCE_BINDING_TIER</a>-typed value that indicates the tier level.
          


### -field PSSpecifiedStencilRefSupported

Specifies whether pixel shader stencil ref is supported. If <b>TRUE</b>, it's supported; otherwise <b>FALSE</b>.
          


### -field TypedUAVLoadAdditionalFormats

Specifies whether the loading of additional formats for typed unordered-access views (UAVs) is supported.
            If <b>TRUE</b>, it's supported; otherwise <b>FALSE</b>.
          


### -field ROVsSupported

Specifies whether <a href="https://msdn.microsoft.com/en-us/library/Dn899119(v=VS.85).aspx">Rasterizer Order Views</a> (ROVs) are supported. If <b>TRUE</b>, they're supported; otherwise <b>FALSE</b>.
          


### -field ConservativeRasterizationTier

Specifies the level at which the hardware and driver support conservative rasterization. The runtime sets this member to a <a href="https://msdn.microsoft.com/en-us/library/Dn859368(v=VS.85).aspx">D3D12_CONSERVATIVE_RASTERIZATION_TIER</a>-typed value that indicates the tier level.
          


### -field MaxGPUVirtualAddressBitsPerResource

Don't use this field; instead, use the <a href="https://msdn.microsoft.com/en-us/library/Mt186607(v=VS.85).aspx">D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</a> query
            (a structure with a <b>MaxGPUVirtualAddressBitsPerResource</b> member), which is more accurate.
            


### -field StandardSwizzle64KBSupported

TRUE if the hardware supports textures with the 64KB standard swizzle pattern.
            Support for this pattern enables zero-copy texture optimizations while providing near-equilateral locality for each dimension within the texture.
            For texture swizzle options and restrictions, see <a href="https://msdn.microsoft.com/en-us/library/Dn770442(v=VS.85).aspx">D3D12_TEXTURE_LAYOUT</a>.
          


### -field CrossNodeSharingTier

A <a href="https://msdn.microsoft.com/en-us/library/Dn914408(v=VS.85).aspx">D3D12_CROSS_NODE_SHARING_TIER</a> enumeration constant that specifies the level of sharing across nodes of an adapter that has multiple nodes,
            such as Tier 1 Emulated, Tier 1, or Tier 2.
          


### -field CrossAdapterRowMajorTextureSupported

FALSE means the device only supports copy operations to and from cross-adapter row-major textures.
            TRUE means the device supports shader resource views, unordered access views, and render target views of cross-adapter row-major textures.
            "Cross-adapter" means between multiple adapters (even from different IHVs).
          


### -field VPAndRTArrayIndexFromAnyShaderFeedingRasterizerSupportedWithoutGSEmulation

Whether the viewport (VP) and Render Target (RT) array index from any shader feeding the rasterizer are supported without geometry shader emulation.
            Compare the <b>VPAndRTArrayIndexFromAnyShaderFeedingRasterizer</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Dn933226(v=VS.85).aspx">D3D11_FEATURE_DATA_D3D11_OPTIONS3</a> structure.
            In <a href="https://msdn.microsoft.com/en-us/library/Dn933714(v=VS.85).aspx">ID3D12ShaderReflection::GetRequiresFlags</a>, see the #define D3D_SHADER_REQUIRES_VIEWPORT_AND_RT_ARRAY_INDEX_FROM_ANY_SHADER_FEEDING_RASTERIZER.
          


### -field ResourceHeapTier

Specifies the level at which the hardware and driver require heap attribution related to resource type.
            The runtime sets this member to a <a href="https://msdn.microsoft.com/en-us/library/Dn986743(v=VS.85).aspx">D3D12_RESOURCE_HEAP_TIER</a> enumeration constant.
          


## -remarks



See <a href="https://msdn.microsoft.com/en-us/library/Dn770363(v=VS.85).aspx">D3D12_FEATURE</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn903791(v=VS.85).aspx">Conservative Rasterization</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn770459(v=VS.85).aspx">Core Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn770363(v=VS.85).aspx">D3D12_FEATURE</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn903929(v=VS.85).aspx">Rasterizer Ordered Views</a>
 

 

