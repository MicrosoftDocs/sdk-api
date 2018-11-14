---
UID: NS:d3d11.D3D11_FEATURE_DATA_MARKER_SUPPORT
title: D3D11_FEATURE_DATA_MARKER_SUPPORT
author: windows-sdk-content
description: Describes whether a GPU profiling technique is supported.
old-location: direct3d11\d3d11_feature_data_marker_support.htm
tech.root: direct3d11
ms.assetid: 950381BB-E8F6-416D-8F36-CC3591E71703
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D11_FEATURE_DATA_MARKER_SUPPORT, D3D11_FEATURE_DATA_MARKER_SUPPORT structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_MARKER_SUPPORT, direct3d11.d3d11_feature_data_marker_support
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - D3D11.h
api_name:
 - D3D11_FEATURE_DATA_MARKER_SUPPORT
product: Windows
targetos: Windows
req.typenames: D3D11_FEATURE_DATA_MARKER_SUPPORT
req.redist: 
---

# D3D11_FEATURE_DATA_MARKER_SUPPORT structure


## -description


<div class="alert"><b>Note</b>  This structure is supported by the Direct3D 11.2 runtime, which is available on Windows 8.1 and later operating systems.</div><div> </div>Describes whether a GPU profiling technique is supported.


## -struct-fields




### -field Profile

Specifies whether the hardware and driver support a GPU profiling technique that can be used with development tools. The runtime sets this member to <b>TRUE</b> if  the hardware and driver support data marking.


## -remarks



If the Direct3D API is the Direct3D 11.2 runtime and can support 11.2 features, <a href="https://msdn.microsoft.com/7edf2ffd-908a-4cf8-9ac6-8fd14d7a0ea1">ID3D11Device::CheckFeatureSupport</a> for <b>D3D11_FEATURE_MARKER_SUPPORT</b> will return a SUCCESS code when valid parameters are passed. The <b>Profile</b> member of <b>D3D11_FEATURE_DATA_MARKER_SUPPORT</b> will be set to <b>TRUE</b> or <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>



<a href="https://msdn.microsoft.com/48c3bf65-f077-45e6-a306-03d5760eeccb">D3D11_FEATURE</a>
 

 

