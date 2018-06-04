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
 

 

