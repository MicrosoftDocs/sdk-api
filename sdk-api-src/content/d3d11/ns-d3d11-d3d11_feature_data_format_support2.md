---
UID: NS:d3d11.D3D11_FEATURE_DATA_FORMAT_SUPPORT2
title: D3D11_FEATURE_DATA_FORMAT_SUPPORT2
author: windows-sdk-content
description: Describes which unordered resource options are supported by the current graphics driver for a given format.
old-location: direct3d11\d3d11_feature_data_format_support2.htm
tech.root: direct3d11
ms.assetid: 075cc44a-3c91-4015-af7f-489b3b3c6661
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 666f73ad-8c04-9774-e3ed-01d758bb509f, D3D11_FEATURE_DATA_FORMAT_SUPPORT2, D3D11_FEATURE_DATA_FORMAT_SUPPORT2 structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_FORMAT_SUPPORT2, direct3d11.d3d11_feature_data_format_support2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - D3D11.h
api_name:
 - D3D11_FEATURE_DATA_FORMAT_SUPPORT2
product: Windows
targetos: Windows
req.typenames: D3D11_FEATURE_DATA_FORMAT_SUPPORT2
req.redist: 
---

# D3D11_FEATURE_DATA_FORMAT_SUPPORT2 structure


## -description


Describes which unordered resource options are supported by the current graphics driver for a given format.


## -struct-fields




### -field InFormat

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> to return information on.


### -field OutFormatSupport2

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Combination of <a href="https://msdn.microsoft.com/en-us/library/Ff476135(v=VS.85).aspx">D3D11_FORMAT_SUPPORT2</a> flags indicating which unordered resource options are supported.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476155(v=VS.85).aspx">Core Structures</a>
 

 

