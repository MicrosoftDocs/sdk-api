---
UID: NE:dxgi1_6.DXGI_GPU_PREFERENCE
title: DXGI_GPU_PREFERENCE
author: windows-sdk-content
description: The preference of GPU for the app to run on.
old-location: direct3ddxgi\dxgi_gpu_preference.htm
old-project: direct3ddxgi
ms.assetid: 4228FF8B-968B-42B5-8355-226C7FE9F230
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: DXGI_GPU_PREFERENCE, DXGI_GPU_PREFERENCE enumeration [DXGI], DXGI_GPU_PREFERENCE_HIGH_PERFORMANCE, DXGI_GPU_PREFERENCE_MINIMUM_POWER, DXGI_GPU_PREFERENCE_UNSPECIFIED, direct3ddxgi.dxgi_gpu_preference, dxgi1_6/DXGI_GPU_PREFERENCE, dxgi1_6/DXGI_GPU_PREFERENCE_HIGH_PERFORMANCE, dxgi1_6/DXGI_GPU_PREFERENCE_MINIMUM_POWER, dxgi1_6/DXGI_GPU_PREFERENCE_UNSPECIFIED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dxgi1_6.h
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
req.typenames: DXGI_GPU_PREFERENCE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_6.h
api_name:
 - DXGI_GPU_PREFERENCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_GPU_PREFERENCE enumeration


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

The preference of GPU for the app to run on.


## -enum-fields




### -field DXGI_GPU_PREFERENCE_UNSPECIFIED

No preference of GPU.


### -field DXGI_GPU_PREFERENCE_MINIMUM_POWER

Preference for the minimum-powered GPU (such as an integrated graphics processor, or iGPU).


### -field DXGI_GPU_PREFERENCE_HIGH_PERFORMANCE

Preference for the highest performing GPU, such as a discrete graphics processor (dGPU) or external graphics processor (xGPU).


## -remarks



This enumeration is used in the <a href="https://msdn.microsoft.com/E5F835FB-3699-4E27-B990-4C1CF6E6DD48">IDXGIFactory6::EnumAdapterByGpuPreference</a> method.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>



<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/UWP/D3D12xGPU">xGPU UWP sample</a>



<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12xGPU">xGPU desktop sample</a>
 

 

