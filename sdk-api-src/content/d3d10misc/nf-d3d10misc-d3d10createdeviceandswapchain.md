---
UID: NF:d3d10misc.D3D10CreateDeviceAndSwapChain
title: D3D10CreateDeviceAndSwapChain function (d3d10misc.h)
author: windows-sdk-content
description: Create a Direct3D 10.0 device and a swap chain.
old-location: direct3d10\d3d10createdeviceandswapchain.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createdeviceandswapchain.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D10CreateDeviceAndSwapChain, D3D10CreateDeviceAndSwapChain function [Direct3D 10], d3d10misc/D3D10CreateDeviceAndSwapChain, direct3d10.d3d10createdeviceandswapchain, f04f4a8c-494a-567c-ed62-cfe70d6e9474
ms.topic: function
f1_keywords: 
 - "d3d10misc/D3D10CreateDeviceAndSwapChain"
dev_langs:
 - c++
req.header: d3d10misc.h
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
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10CreateDeviceAndSwapChain
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# D3D10CreateDeviceAndSwapChain function


## -description


Create a Direct3D 10.0 device and a swap chain.


## -parameters




### -param pAdapter [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>.


### -param DriverType [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type">D3D10_DRIVER_TYPE</a></b>

The type of driver for the device. See <a href="https://docs.microsoft.com/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type">D3D10_DRIVER_TYPE</a>.


### -param Software [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HMODULE</a></b>

A handle to the DLL that implements a software rasterizer. Must be <b>NULL</b> if DriverType is non-software. The HMODULE of a DLL can be obtained with <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>, <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>.


### -param Flags [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Optional. Device creation flags (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag">D3D10_CREATE_DEVICE_FLAG</a>) that enable <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers">API layers</a>. These flags can be bitwise OR'd together.


### -param SDKVersion [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Bit flag that indicates the version of the SDK. Should be D3D10_SDK_VERSION, defined in d3d10.h.


### -param pSwapChainDesc [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc">DXGI_SWAP_CHAIN_DESC</a>*</b>

Description of the swap chain. See <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc">DXGI_SWAP_CHAIN_DESC</a>.


### -param ppSwapChain [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>**</b>

Address of a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>.


### -param ppDevice [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>**</b>

Address of a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a> that will receive the newly created device.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -remarks



To create a device without creating a swap chain, see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice">D3D10CreateDevice</a>.

<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-functions">Core Functions</a>
 

 

