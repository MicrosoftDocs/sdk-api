---
UID: NS:d3d11.D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT
title: D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT
author: windows-sdk-content
description: Describes whether simple instancing is supported.
old-location: direct3d11\d3d11_feature_data_d3d9_simple_instancing_support.htm
old-project: direct3d11
ms.assetid: 940381BB-E8F6-416D-8F36-CC3591E70703
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT, D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT, direct3d11.d3d11_feature_data_d3d9_simple_instancing_support
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
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
req.typenames: D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT structure


## -description


<div class="alert"><b>Note</b>  
        This structure is supported by the Direct3D 11.2 runtime, which is available on Windows 8.1 and later operating systems.
      </div><div> </div>Describes whether simple instancing is supported.


## -struct-fields




### -field SimpleInstancingSupported


            Specifies whether the hardware and driver support simple instancing. The runtime sets this member to <b>TRUE</b> if  the hardware and driver support simple instancing.
          


## -remarks




        If the Direct3D API is the Direct3D 11.2 runtime and can support 11.2 features, <a href="https://msdn.microsoft.com/7edf2ffd-908a-4cf8-9ac6-8fd14d7a0ea1">ID3D11Device::CheckFeatureSupport</a> for <b>D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT</b> will return a SUCCESS code when valid parameters are passed. The <b>SimpleInstancingSupported</b> member of <b>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</b> will be set to <b>TRUE</b> or <b>FALSE</b>.
      


        Simple instancing means that instancing is supported with the caveat that the <b>InstanceDataStepRate</b> member of the <a href="https://msdn.microsoft.com/45545d24-1513-4efd-9344-20673c5b98d5">D3D11_INPUT_ELEMENT_DESC</a> structure must be equal to 1. This does not change the full instancing support provided by hardware at feature level 9.3 and above, and is meant to expose the instancing support that may be available on feature level 9.2 and 9.1 hardware.
      




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>



<a href="https://msdn.microsoft.com/48c3bf65-f077-45e6-a306-03d5760eeccb">D3D11_FEATURE</a>
 

 

