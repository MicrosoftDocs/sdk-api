---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS2
title: D3D12_FEATURE_DATA_D3D12_OPTIONS2
author: windows-sdk-content
description: Details the adapter's support for certain optional features of Direct3D 12.
old-location: direct3d12\d3d12_feature_data_d3d12_options2.htm
tech.root: direct3d12
ms.assetid: E45DA471-E0A9-47BF-8AE5-4B8BA4B38337
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: D3D12_FEATURE_DATA_D3D12_OPTIONS2, D3D12_FEATURE_DATA_D3D12_OPTIONS2 structure, d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS2, direct3d12.d3d12_feature_data_d3d12_options2
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
 - D3D12_FEATURE_DATA_D3D12_OPTIONS2
product: Windows
targetos: Windows
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS2
req.redist: 
---

# D3D12_FEATURE_DATA_D3D12_OPTIONS2 structure


## -description


Details the adapter's support for certain optional features of Direct3D 12.


## -struct-fields




### -field DepthBoundsTestSupported

<a href="https://msdn.microsoft.com/en-us/library/jj159528.aspx">SAL</a>: <code>_Out_</code>

On return, contains true if depth-bounds tests are supported; otherwise, false.


### -field ProgrammableSamplePositionsTier

<a href="https://msdn.microsoft.com/en-us/library/jj159528.aspx">SAL</a>: <code>_Out_</code>

On return, contains a value that indicates the level of support offered for programmable sample positions.


## -remarks



Use this structure with <a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">CheckFeatureSupport</a> to determine the level of support offered for the optional Depth-bounds test and programmable sample positions features.

See the enumeration constant D3D12_FEATURE_D3D12_OPTIONS2 in the <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

