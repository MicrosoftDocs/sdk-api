---
UID: NS:d3d12.D3D12_FEATURE_DATA_SHADER_CACHE
title: D3D12_FEATURE_DATA_SHADER_CACHE (d3d12.h)
author: windows-sdk-content
description: Describes the level of shader caching supported in the current graphics driver.
old-location: direct3d12\d3d12_feature_data_shader_cache.htm
tech.root: direct3d12
ms.assetid: B6BC2E8F-04FE-4855-87C2-89A054519AFD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_FEATURE_DATA_SHADER_CACHE, D3D12_FEATURE_DATA_SHADER_CACHE structure, d3d12/D3D12_FEATURE_DATA_SHADER_CACHE, direct3d12.d3d12_feature_data_shader_cache
ms.topic: struct
f1_keywords: ["d3d12/D3D12_FEATURE_DATA_SHADER_CACHE"]
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
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_SHADER_CACHE
product: Windows
targetos: Windows
req.typenames: D3D12_FEATURE_DATA_SHADER_CACHE
req.redist: 
ms.custom: 19H1
---

# D3D12_FEATURE_DATA_SHADER_CACHE structure


## -description


Describes the level of shader caching supported in the current graphics driver.


## -struct-fields




### -field SupportFlags

<a href="https://docs.microsoft.com/visualstudio/code-quality/annotating-structs-and-classes?view=vs-2015">SAL</a>: <code>_Out_</code>

Indicates the level of caching supported.


## -remarks



Use this structure with <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport">CheckFeatureSupport</a> to determine the level of support offered for the optional shader-caching features.

See the enumeration constant D3D12_FEATURE_SHADER_CACHE in the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>
 

 

