---
UID: NE:d3d12.D3D12_FEATURE
title: D3D12_FEATURE
author: windows-sdk-content
description: Direct3D 12 feature options that are supported by the current graphics driver.
old-location: direct3d12\d3d12_feature.htm
old-project: direct3d12
ms.assetid: 165ECFE0-1B18-4A26-8B9C-3CE53776A349
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: D3D12_FEATURE, D3D12_FEATURE enumeration, D3D12_FEATURE_ARCHITECTURE, D3D12_FEATURE_ARCHITECTURE1, D3D12_FEATURE_COMMAND_QUEUE_PRIORITY, D3D12_FEATURE_D3D12_OPTIONS, D3D12_FEATURE_D3D12_OPTIONS1, D3D12_FEATURE_D3D12_OPTIONS2, D3D12_FEATURE_D3D12_OPTIONS3, D3D12_FEATURE_EXISTING_HEAPS, D3D12_FEATURE_FEATURE_LEVELS, D3D12_FEATURE_FORMAT_INFO, D3D12_FEATURE_FORMAT_SUPPORT, D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT, D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS, D3D12_FEATURE_ROOT_SIGNATURE, D3D12_FEATURE_SHADER_CACHE, D3D12_FEATURE_SHADER_MODEL, d3d12/D3D12_FEATURE, d3d12/D3D12_FEATURE_ARCHITECTURE, d3d12/D3D12_FEATURE_ARCHITECTURE1, d3d12/D3D12_FEATURE_COMMAND_QUEUE_PRIORITY, d3d12/D3D12_FEATURE_D3D12_OPTIONS, d3d12/D3D12_FEATURE_D3D12_OPTIONS1, d3d12/D3D12_FEATURE_D3D12_OPTIONS2, d3d12/D3D12_FEATURE_D3D12_OPTIONS3, d3d12/D3D12_FEATURE_EXISTING_HEAPS, d3d12/D3D12_FEATURE_FEATURE_LEVELS, d3d12/D3D12_FEATURE_FORMAT_INFO, d3d12/D3D12_FEATURE_FORMAT_SUPPORT, d3d12/D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT, d3d12/D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS, d3d12/D3D12_FEATURE_ROOT_SIGNATURE, d3d12/D3D12_FEATURE_SHADER_CACHE, d3d12/D3D12_FEATURE_SHADER_MODEL, direct3d12.d3d12_feature
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D12_FEATURE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D12.h
api_name:
-	D3D12_FEATURE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_FEATURE enumeration


## -description



          Direct3D 12 feature options that are supported by the current graphics driver.
        


## -enum-fields




### -field D3D12_FEATURE_D3D12_OPTIONS


            Supports Direct3D 12 feature options described in <a href="https://msdn.microsoft.com/3193E3CC-C6CA-43D4-8D8C-41B7FCEE2BDF">D3D12_FEATURE_DATA_D3D12_OPTIONS</a>.
          


### -field D3D12_FEATURE_ARCHITECTURE


            Describes each GPUs' architectural details on the adapter described in <a href="https://msdn.microsoft.com/FA16A260-3CC9-4F32-A97B-8A561A01C138">D3D12_FEATURE_DATA_ARCHITECTURE</a>.


### -field D3D12_FEATURE_FEATURE_LEVELS


              Supports specific <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature levels</a>, described in 
            <a href="https://msdn.microsoft.com/8C709889-0C7E-4D6D-84BD-1449BB8EA96A">D3D12_FEATURE_DATA_FEATURE_LEVELS</a>.


### -field D3D12_FEATURE_FORMAT_SUPPORT


            Supports resources for a specific format, described in <a href="https://msdn.microsoft.com/6E4EB08F-0B60-4B1E-AD27-8F0AE2BD0766">D3D12_FEATURE_DATA_FORMAT_SUPPORT</a>.


### -field D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS


              Supports image quality levels for a specific format and sample count, described in 
            <a href="https://msdn.microsoft.com/F3ECEF7C-F4A4-4134-9671-21AE488D8183">D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS</a>.


### -field D3D12_FEATURE_FORMAT_INFO


            Supports DXGI_FORMAT and the number of planes to provide information about, described in 
          <a href="https://msdn.microsoft.com/8695994A-CC83-451C-AD1B-65359656F3CC">D3D12_FEATURE_DATA_FORMAT_INFO</a>.


### -field D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT


            Supports GPU virtual addresses, described in 
          <a href="https://msdn.microsoft.com/2CBED491-A8B6-47AE-8371-2081BAF85B83">D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</a>.


### -field D3D12_FEATURE_SHADER_MODEL


            Supports shader models, described in 
          <a href="https://msdn.microsoft.com/17978B9A-D21B-4A8A-B367-12F4ABC43A94">D3D12_FEATURE_DATA_SHADER_MODEL</a>.


### -field D3D12_FEATURE_D3D12_OPTIONS1


          Check for support options described in <a href="https://msdn.microsoft.com/39BF7632-AC73-471B-94F9-3128BD0DAB89">D3D12_FEATURE_DATA_D3D12_OPTIONS1</a>.


### -field D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT


### -field D3D12_FEATURE_ROOT_SIGNATURE


          Supports root signature versions, described in <a href="https://msdn.microsoft.com/3CC49B10-18B9-4A10-9013-D8F265FD1A28">D3D12_FEATURE_DATA_ROOT_SIGNATURE</a>.


### -field D3D12_FEATURE_ARCHITECTURE1


            Describes each GPUs' architectural details on the adapter described in <a href="https://msdn.microsoft.com/635091FE-2756-4648-958E-0C13BDD50851">D3D12_FEATURE_DATA_ARCHITECTURE1</a>.


### -field D3D12_FEATURE_D3D12_OPTIONS2


          Check for support options described in <a href="https://msdn.microsoft.com/E45DA471-E0A9-47BF-8AE5-4B8BA4B38337">D3D12_FEATURE_DATA_D3D12_OPTIONS2</a>.


### -field D3D12_FEATURE_SHADER_CACHE


            Supports shader cache, described in 
          <a href="https://msdn.microsoft.com/B6BC2E8F-04FE-4855-87C2-89A054519AFD">D3D12_FEATURE_DATA_SHADER_CACHE</a>.


### -field D3D12_FEATURE_COMMAND_QUEUE_PRIORITY


            Supports command-queue priorities, described in 
          <a href="https://msdn.microsoft.com/70DB58DB-7EE0-4E5C-8B24-22DA9347A80F">D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY</a>.


### -field D3D12_FEATURE_D3D12_OPTIONS3


            Check for support options described in <a href="https://msdn.microsoft.com/E45DA471-E0A9-47BF-8AE5-4B8BA4B38337">D3D12_FEATURE_DATA_D3D12_OPTIONS2</a>.


### -field D3D12_FEATURE_EXISTING_HEAPS


	    Supports existing heaps, described in 
          <a href="https://msdn.microsoft.com/7F0D0FAD-BF29-43AD-95FA-85B9719C4782">D3D12_FEATURE_DATA_EXISTING_HEAPS</a>.
          


### -field D3D12_FEATURE_D3D12_OPTIONS4


### -field D3D12_FEATURE_SERIALIZATION


### -field D3D12_FEATURE_CROSS_NODE




## -remarks




        Use this enumeration in a call to <a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">ID3D12Device::CheckFeatureSupport</a> to query a driver about support for the Direct3D 12 features.
        Each value in this enumeration has a corresponding data structure that you must pass to the <i>pFeatureSupportData</i> parameter
        of <b>ID3D12Device::CheckFeatureSupport</b>.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

