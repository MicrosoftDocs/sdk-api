---
UID: NE:d3d11.D3D11_SHADER_CACHE_SUPPORT_FLAGS
title: D3D11_SHADER_CACHE_SUPPORT_FLAGS
author: windows-sdk-content
description: Describes the level of support for shader caching in the current graphics driver.
old-location: direct3d11\d3d11_shader_cache_support_flags.htm
tech.root: direct3d11
ms.assetid: FC5B37C0-8512-441B-AC33-FAE378C8C3EC
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D3D11_SHADER_CACHE_SUPPORT_AUTOMATIC_DISK_CACHE, D3D11_SHADER_CACHE_SUPPORT_AUTOMATIC_INPROC_CACHE, D3D11_SHADER_CACHE_SUPPORT_FLAGS, D3D11_SHADER_CACHE_SUPPORT_FLAGS enumeration [Direct3D 11], D3D11_SHADER_CACHE_SUPPORT_NONE, d3d11/D3D11_SHADER_CACHE_SUPPORT_AUTOMATIC_DISK_CACHE, d3d11/D3D11_SHADER_CACHE_SUPPORT_AUTOMATIC_INPROC_CACHE, d3d11/D3D11_SHADER_CACHE_SUPPORT_FLAGS, d3d11/D3D11_SHADER_CACHE_SUPPORT_NONE, direct3d11.d3d11_shader_cache_support_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d11.h
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
 - d3d11.h
api_name:
 - D3D11_SHADER_CACHE_SUPPORT_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D11_SHADER_CACHE_SUPPORT_FLAGS
req.redist: 
---

# D3D11_SHADER_CACHE_SUPPORT_FLAGS enumeration


## -description


Describes the level of support for shader caching in the current graphics driver.


## -enum-fields




### -field D3D11_SHADER_CACHE_SUPPORT_NONE

Indicates that the driver does not support shader caching.


### -field D3D11_SHADER_CACHE_SUPPORT_AUTOMATIC_INPROC_CACHE

Indicates that the driver supports an OS-managed shader cache that stores compiled shaders in memory during the current run of the application.


### -field D3D11_SHADER_CACHE_SUPPORT_AUTOMATIC_DISK_CACHE

Indicates that the driver supports an OS-managed shader cache that stores compiled shaders on disk to accelerate future runs of the application.


## -remarks



This enum is used by the <a href="direct3d11d3d11_feature_data_shader_cache">D3D_FEATURE_DATA_SHADER_CACHE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476155(v=VS.85).aspx">Core Structures</a>
 

 

