---
UID: NE:d3d12.D3D12_SHADER_CACHE_SUPPORT_FLAGS
title: D3D12_SHADER_CACHE_SUPPORT_FLAGS
author: windows-driver-content
description: Describes the level of support for shader caching in the current graphics driver.
old-location: direct3d12\d3d12_shader_cache_support_flags.htm
old-project: direct3d12
ms.assetid: E270E04A-769F-4B08-AC17-5A87430CB3DA
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: D3D12_SHADER_CACHE_SUPPORT_AUTOMATIC_DISK_CACHE, D3D12_SHADER_CACHE_SUPPORT_AUTOMATIC_INPROC_CACHE, D3D12_SHADER_CACHE_SUPPORT_FLAGS, D3D12_SHADER_CACHE_SUPPORT_FLAGS enumeration, D3D12_SHADER_CACHE_SUPPORT_LIBRARY, D3D12_SHADER_CACHE_SUPPORT_NONE, D3D12_SHADER_CACHE_SUPPORT_SINGLE_PSO, d3d12/D3D12_SHADER_CACHE_SUPPORT_AUTOMATIC_DISK_CACHE, d3d12/D3D12_SHADER_CACHE_SUPPORT_AUTOMATIC_INPROC_CACHE, d3d12/D3D12_SHADER_CACHE_SUPPORT_FLAGS, d3d12/D3D12_SHADER_CACHE_SUPPORT_LIBRARY, d3d12/D3D12_SHADER_CACHE_SUPPORT_NONE, d3d12/D3D12_SHADER_CACHE_SUPPORT_SINGLE_PSO, direct3d12.d3d12_shader_cache_support_flags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: D3D12_SHADER_CACHE_SUPPORT_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d12.h
api_name:
-	D3D12_SHADER_CACHE_SUPPORT_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_SHADER_CACHE_SUPPORT_FLAGS enumeration


## -description


Describes the level of support for shader caching in the current graphics driver.


## -enum-fields




### -field D3D12_SHADER_CACHE_SUPPORT_NONE

Indicates that the driver does not support shader caching.


### -field D3D12_SHADER_CACHE_SUPPORT_SINGLE_PSO

Indicates that the driver supports the CachedPSO member of the <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> and <a href="https://msdn.microsoft.com/46C785C6-8294-410F-A8D5-7E5F85FA5C75">D3D12_COMPUTE_PIPELINE_STATE_DESC</a> structures. This is always supported.


### -field D3D12_SHADER_CACHE_SUPPORT_LIBRARY

Indicates that the driver supports the ID3D12PipelineLibrary interface, which provides application-controlled PSO grouping and caching. This is supported by drivers targetting the Windows 10 Anniversary Update.


### -field D3D12_SHADER_CACHE_SUPPORT_AUTOMATIC_INPROC_CACHE

Indicates that the driver supports an OS-managed shader cache that stores compiled shaders in memory during the current run of the application.


### -field D3D12_SHADER_CACHE_SUPPORT_AUTOMATIC_DISK_CACHE

Indicates that the driver supports an OS-managed shader cache that stores compiled shaders on disk to accelerate future runs of the application.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/B6BC2E8F-04FE-4855-87C2-89A054519AFD">D3D_FEATURE_DATA_SHADER_CACHE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

