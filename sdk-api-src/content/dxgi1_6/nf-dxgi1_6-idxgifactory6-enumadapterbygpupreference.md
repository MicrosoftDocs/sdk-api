---
UID: NF:dxgi1_6.IDXGIFactory6.EnumAdapterByGpuPreference
title: IDXGIFactory6::EnumAdapterByGpuPreference
author: windows-sdk-content
description: Enumerates graphics adapters based on a given GPU preference.
old-location: direct3ddxgi\idxgifactory6_enumadapterbygpupreference.htm
old-project: direct3ddxgi
ms.assetid: E5F835FB-3699-4E27-B990-4C1CF6E6DD48
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: EnumAdapterByGpuPreference, EnumAdapterByGpuPreference method [DXGI], EnumAdapterByGpuPreference method [DXGI],IDXGIFactory6 interface, IDXGIFactory6 interface [DXGI],EnumAdapterByGpuPreference method, IDXGIFactory6.EnumAdapterByGpuPreference, IDXGIFactory6::EnumAdapterByGpuPreference, direct3ddxgi.idxgifactory6_enumadapterbygpupreference, dxgi1_6/IDXGIFactory6::EnumAdapterByGpuPreference
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS
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
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIFactory6::EnumAdapterByGpuPreference


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Enumerates graphics adapters based on a given GPU preference.


## -parameters




### -param Adapter [in]

Type: <b>UINT</b>

The index of the adapter to enumerate. The indices are in order of the preference specified in <i>GpuPreference</i>—for example, if <b>DXGI_GPU_PREFERENCE_HIGH_PERFORMANCE</b> is specified, then the highest-performing adapter is at index 0, the second-highest is at index 1, and so on.


### -param GpuPreference [in]

Type: <b><a href="https://msdn.microsoft.com/4228FF8B-968B-42B5-8355-226C7FE9F230">DXGI_GPU_PREFERENCE</a></b>

The GPU preference for the app.


### -param riid [in]

Type: <b>REFIID</b>

The globally unique identifier (GUID) of the <a href="https://msdn.microsoft.com/CB4BC8A4-D5D5-48B9-A477-65A12A43D4A6">IDXGIAdapter</a> object referenced by the <i>ppvAdapter</i> parameter.


### -param ppvAdapter [out]

Type: <b>void**</b>

            The address of an <a href="https://msdn.microsoft.com/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a> interface pointer to the adapter.
            This parameter must not be NULL.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.




## -remarks



This method allows developers to select which GPU they think is most appropriate for each device their app creates and utilizes.

This method is similar to <a href="https://msdn.microsoft.com/AC800F32-2922-45BA-A6D3-D3E45113B9A7">IDXGIFactory4::EnumAdapterByLuid</a>, but it accepts a GPU preference instead of an adapter LUID. It returns the appropriate <b>IDXGIAdapter</b> for the given GPU preference. It is meant to be used in conjunction with the <b>D3D*CreateDevice</b> functions, which take in an <b>IDXGIAdapter*</b>.

When <b>DXGI_GPU_PREFERENCE_UNSPECIFIED</b> is specified for the <i>GpuPreference</i> parameter, this method is equivalent to calling <a href="https://msdn.microsoft.com/351b7b2d-abb7-449e-bee2-eea96fef3b9d">IDXGIFactory1::EnumAdapters1</a>.

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




<a href="https://msdn.microsoft.com/CB4BC8A4-D5D5-48B9-A477-65A12A43D4A6">IDXGIFactory6</a>



<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/UWP/D3D12xGPU">xGPU UWP sample</a>



<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12xGPU">xGPU desktop sample</a>
 

 

