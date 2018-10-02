---
UID: NS:d3d11.D3D11_FEATURE_DATA_SHADER_CACHE
title: D3D11_FEATURE_DATA_SHADER_CACHE
author: windows-sdk-content
description: Describes the level of shader caching supported in the current graphics driver.
old-location: direct3d11\d3d11_feature_data_shader_cache.htm
tech.root: direct3d11
ms.assetid: 45F1184E-0E82-4AF4-86F7-ED0E4C860026
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D11_FEATURE_DATA_SHADER_CACHE, D3D11_FEATURE_DATA_SHADER_CACHE structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_SHADER_CACHE, direct3d11.d3d11_feature_data_shader_cache
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
req.include-header: D3d11_3.h
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
 - d3d11.h
api_name:
 - D3D11_FEATURE_DATA_SHADER_CACHE
product: Windows
targetos: Windows
req.typenames: D3D11_FEATURE_DATA_SHADER_CACHE
req.redist: 
---

# D3D11_FEATURE_DATA_SHADER_CACHE structure


## -description


Describes the level of shader caching supported in the current graphics driver.


## -struct-fields




### -field SupportFlags

Indicates the level of caching supported.


## -remarks



Use this structure with <a href="https://msdn.microsoft.com/7edf2ffd-908a-4cf8-9ac6-8fd14d7a0ea1">CheckFeatureSupport</a> to determine the level of support offered for the optional shader-caching features.

See the enumeration constant D3D11_FEATURE_SHADER_CACHE in the <a href="https://msdn.microsoft.com/48c3bf65-f077-45e6-a306-03d5760eeccb">D3D11_FEATURE</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

