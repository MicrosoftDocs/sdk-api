---
UID: NS:d3d12.D3D12_FEATURE_DATA_SHADER_CACHE
title: D3D12_FEATURE_DATA_SHADER_CACHE
author: windows-sdk-content
description: Describes the level of shader caching supported in the current graphics driver.
old-location: direct3d12\d3d12_feature_data_shader_cache.htm
tech.root: direct3d12
ms.assetid: B6BC2E8F-04FE-4855-87C2-89A054519AFD
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: D3D12_FEATURE_DATA_SHADER_CACHE, D3D12_FEATURE_DATA_SHADER_CACHE structure, d3d12/D3D12_FEATURE_DATA_SHADER_CACHE, direct3d12.d3d12_feature_data_shader_cache
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
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_SHADER_CACHE
product: Windows
targetos: Windows
req.typenames: D3D12_FEATURE_DATA_SHADER_CACHE
req.redist: 
---

# D3D12_FEATURE_DATA_SHADER_CACHE structure


## -description


Describes the level of shader caching supported in the current graphics driver.


## -struct-fields




### -field SupportFlags

<a href="https://msdn.microsoft.com/en-us/library/jj159528.aspx">SAL</a>: <code>_Out_</code>

Indicates the level of caching supported.


## -remarks



Use this structure with <a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">CheckFeatureSupport</a> to determine the level of support offered for the optional shader-caching features.

See the enumeration constant D3D12_FEATURE_SHADER_CACHE in the <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

