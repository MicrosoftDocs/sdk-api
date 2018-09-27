---
UID: NS:d3d11.D3D11_FEATURE_DATA_ARCHITECTURE_INFO
title: D3D11_FEATURE_DATA_ARCHITECTURE_INFO
author: windows-sdk-content
description: Describes information about Direct3D 11.1 adapter architecture.
old-location: direct3d11\d3d11_feature_data_architecture_info.htm
tech.root: direct3d11
ms.assetid: BC815FDB-984C-4857-AF48-8B471F46CDD4
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: D3D11_FEATURE_DATA_ARCHITECTURE_INFO, D3D11_FEATURE_DATA_ARCHITECTURE_INFO structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_ARCHITECTURE_INFO, direct3d11.d3d11_feature_data_architecture_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - D3D11_FEATURE_DATA_ARCHITECTURE_INFO
product: Windows
targetos: Windows
req.typenames: D3D11_FEATURE_DATA_ARCHITECTURE_INFO
req.redist: 
---

# D3D11_FEATURE_DATA_ARCHITECTURE_INFO structure


## -description


<div class="alert"><b>Note</b>  This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</div><div> </div>Describes information about Direct3D 11.1 adapter architecture.


## -struct-fields




### -field TileBasedDeferredRenderer

Specifies whether a rendering device batches rendering commands and performs multipass rendering into tiles or bins over a render area. Certain API usage patterns that are fine for TileBasedDefferredRenderers (TBDRs) can perform worse on non-TBDRs and vice versa.  Applications that are careful about rendering can be friendly to both TBDR and non-TBDR architectures. <b>TRUE</b> if the rendering device batches rendering commands and <b>FALSE</b> otherwise. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476155(v=VS.85).aspx">Core Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476124(v=VS.85).aspx">D3D11_FEATURE</a>
 

 

