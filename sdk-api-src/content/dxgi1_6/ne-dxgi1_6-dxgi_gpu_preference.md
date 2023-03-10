---
UID: NE:dxgi1_6.DXGI_GPU_PREFERENCE
title: DXGI_GPU_PREFERENCE (dxgi1_6.h)
description: The preference of GPU for the app to run on.
helpviewer_keywords: ["DXGI_GPU_PREFERENCE","DXGI_GPU_PREFERENCE enumeration [DXGI]","DXGI_GPU_PREFERENCE_HIGH_PERFORMANCE","DXGI_GPU_PREFERENCE_MINIMUM_POWER","DXGI_GPU_PREFERENCE_UNSPECIFIED","direct3ddxgi.dxgi_gpu_preference","dxgi1_6/DXGI_GPU_PREFERENCE","dxgi1_6/DXGI_GPU_PREFERENCE_HIGH_PERFORMANCE","dxgi1_6/DXGI_GPU_PREFERENCE_MINIMUM_POWER","dxgi1_6/DXGI_GPU_PREFERENCE_UNSPECIFIED"]
old-location: direct3ddxgi\dxgi_gpu_preference.htm
tech.root: direct3ddxgi
ms.assetid: 4228FF8B-968B-42B5-8355-226C7FE9F230
ms.date: 12/05/2018
ms.keywords: DXGI_GPU_PREFERENCE, DXGI_GPU_PREFERENCE enumeration [DXGI], DXGI_GPU_PREFERENCE_HIGH_PERFORMANCE, DXGI_GPU_PREFERENCE_MINIMUM_POWER, DXGI_GPU_PREFERENCE_UNSPECIFIED, direct3ddxgi.dxgi_gpu_preference, dxgi1_6/DXGI_GPU_PREFERENCE, dxgi1_6/DXGI_GPU_PREFERENCE_HIGH_PERFORMANCE, dxgi1_6/DXGI_GPU_PREFERENCE_MINIMUM_POWER, dxgi1_6/DXGI_GPU_PREFERENCE_UNSPECIFIED
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DXGI_GPU_PREFERENCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_GPU_PREFERENCE
 - dxgi1_6/DXGI_GPU_PREFERENCE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_6.h
api_name:
 - DXGI_GPU_PREFERENCE
---

# DXGI_GPU_PREFERENCE enumeration


## -description



The preference of GPU for the app to run on.

## -enum-fields

### -field DXGI_GPU_PREFERENCE_UNSPECIFIED:0

No preference of GPU.

### -field DXGI_GPU_PREFERENCE_MINIMUM_POWER

Preference for the minimum-powered GPU (such as an integrated graphics processor, or iGPU).

### -field DXGI_GPU_PREFERENCE_HIGH_PERFORMANCE

Preference for the highest performing GPU, such as a discrete graphics processor (dGPU) or external graphics processor (xGPU).

## -remarks

This enumeration is used in the <a href="/windows/desktop/api/dxgi1_6/nf-dxgi1_6-idxgifactory6-enumadapterbygpupreference">IDXGIFactory6::EnumAdapterByGpuPreference</a> method.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>



<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/UWP/D3D12xGPU">xGPU UWP sample</a>



<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12xGPU">xGPU desktop sample</a>
