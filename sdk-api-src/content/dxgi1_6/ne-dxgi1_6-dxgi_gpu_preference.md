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
 

 

