---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

