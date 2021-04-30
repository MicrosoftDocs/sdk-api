---
UID: NF:dxgi1_6.IDXGIFactory6.EnumAdapterByGpuPreference
title: IDXGIFactory6::EnumAdapterByGpuPreference (dxgi1_6.h)
description: Enumerates graphics adapters based on a given GPU preference.
helpviewer_keywords: ["EnumAdapterByGpuPreference","EnumAdapterByGpuPreference method [DXGI]","EnumAdapterByGpuPreference method [DXGI]","IDXGIFactory6 interface","IDXGIFactory6 interface [DXGI]","EnumAdapterByGpuPreference method","IDXGIFactory6.EnumAdapterByGpuPreference","IDXGIFactory6::EnumAdapterByGpuPreference","direct3ddxgi.idxgifactory6_enumadapterbygpupreference","dxgi1_6/IDXGIFactory6::EnumAdapterByGpuPreference"]
old-location: direct3ddxgi\idxgifactory6_enumadapterbygpupreference.htm
tech.root: direct3ddxgi
ms.assetid: E5F835FB-3699-4E27-B990-4C1CF6E6DD48
ms.date: 12/05/2018
ms.keywords: EnumAdapterByGpuPreference, EnumAdapterByGpuPreference method [DXGI], EnumAdapterByGpuPreference method [DXGI],IDXGIFactory6 interface, IDXGIFactory6 interface [DXGI],EnumAdapterByGpuPreference method, IDXGIFactory6.EnumAdapterByGpuPreference, IDXGIFactory6::EnumAdapterByGpuPreference, direct3ddxgi.idxgifactory6_enumadapterbygpupreference, dxgi1_6/IDXGIFactory6::EnumAdapterByGpuPreference
req.header: dxgi1_6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server, version 1709 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIFactory6::EnumAdapterByGpuPreference
 - dxgi1_6/IDXGIFactory6::EnumAdapterByGpuPreference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.lib
 - dxgi.dll
api_name:
 - IDXGIFactory6.EnumAdapterByGpuPreference
---

## -description

Enumerates graphics adapters based on a given GPU preference.

## -parameters

### -param Adapter [in]

Type: <b>UINT</b>

The index of the adapter to enumerate. The indices are in order of the preference specified in <i>GpuPreference</i>—for example, if <b>DXGI_GPU_PREFERENCE_HIGH_PERFORMANCE</b> is specified, then the highest-performing adapter is at index 0, the second-highest is at index 1, and so on.

### -param GpuPreference [in]

Type: <b><a href="/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference">DXGI_GPU_PREFERENCE</a></b>

The GPU preference for the app.

### -param riid [in]

Type: <b>REFIID</b>

The globally unique identifier (GUID) of the <a href="/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory6">IDXGIAdapter</a> object referenced by the <i>ppvAdapter</i> parameter.

### -param ppvAdapter [out]

Type: <b>void**</b>

The address of an <a href="/windows/win32/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a> interface pointer to the adapter.

This parameter must not be NULL.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful; an error code otherwise. For a list of error codes, see <a href="/windows/win32/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

This method allows developers to select which GPU they think is most appropriate for each device their app creates and utilizes.

This method is similar to <a href="/windows/win32/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1">IDXGIFactory1::EnumAdapters1</a>, but it accepts a GPU preference to reorder the adapter enumeration. It returns the appropriate <b>IDXGIAdapter</b> for the given GPU preference. It is meant to be used in conjunction with the <b>D3D*CreateDevice</b> functions, which take in an <b>IDXGIAdapter*</b>.

When <b>DXGI_GPU_PREFERENCE_UNSPECIFIED</b> is specified for the <i>GpuPreference</i> parameter, this method is equivalent to calling <a href="/windows/win32/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1">IDXGIFactory1::EnumAdapters1</a>.

When <b>DXGI_GPU_PREFERENCE_MINIMUM_POWER</b> is specified for the <i>GpuPreference</i> parameter, the order of preference for the adapter returned in <i>ppvAdapter</i> will be:<dl>
<dd>1. iGPUs (integrated GPUs)</dd>
<dd>2. dGPUs (discrete GPUs)</dd>
<dd>3. xGPUs (external GPUs)</dd>
</dl>


When <b>DXGI_GPU_PREFERENCE_HIGH_PERFORMANCE</b> is specified for the <i>GpuPreference</i> parameter, the order of preference for the adapter returned in <i>ppvAdapter</i> will be:<dl>
<dd>1. xGPUs</dd>
<dd>2. dGPUs</dd>
<dd>3. iGPUs</dd>
</dl>

## -see-also

<a href="/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory6">IDXGIFactory6</a>

<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/UWP/D3D12xGPU">xGPU UWP sample</a>

<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12xGPU">xGPU desktop sample</a>

