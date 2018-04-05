---
UID: NS:d3d12.D3D12_FEATURE_DATA_ROOT_SIGNATURE
title: D3D12_FEATURE_DATA_ROOT_SIGNATURE
author: windows-driver-content
description: Pass this structure to CheckFeatureSupport to check for root signature version support.
old-location: direct3d12\d3d12_feature_data_root_signature.htm
old-project: direct3d12
ms.assetid: 3CC49B10-18B9-4A10-9013-D8F265FD1A28
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: D3D12_FEATURE_DATA_ROOT_SIGNATURE, D3D12_FEATURE_DATA_ROOT_SIGNATURE structure, d3d12/D3D12_FEATURE_DATA_ROOT_SIGNATURE, direct3d12.d3d12_feature_data_root_signature
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3D12_FEATURE_DATA_ROOT_SIGNATURE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d12.h
api_name:
-	D3D12_FEATURE_DATA_ROOT_SIGNATURE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_FEATURE_DATA_ROOT_SIGNATURE structure


## -description


Pass this structure to <a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">CheckFeatureSupport</a> to check for root signature version support.


## -struct-fields




### -field HighestVersion

On input, specifies the highest version <a href="https://msdn.microsoft.com/44A22509-5CAE-4C4E-ADC6-E86B5BD8CE3B">D3D_ROOT_SIGNATURE_VERSION</a> to check for. On output specifies the highest version, up to the input version specified, actually available.


## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

