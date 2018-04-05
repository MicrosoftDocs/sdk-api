---
UID: NF:d3d10misc.D3D10CreateDeviceAndSwapChain
title: D3D10CreateDeviceAndSwapChain function
author: windows-driver-content
description: Create a Direct3D 10.0 device and a swap chain.
old-location: direct3d10\d3d10createdeviceandswapchain.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createdeviceandswapchain.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: D3D10CreateDeviceAndSwapChain, D3D10CreateDeviceAndSwapChain function [Direct3D 10], d3d10misc/D3D10CreateDeviceAndSwapChain, direct3d10.d3d10createdeviceandswapchain, f04f4a8c-494a-567c-ed62-cfe70d6e9474
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: D3D10_DRIVER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	D3D10.dll
api_name:
-	D3D10CreateDeviceAndSwapChain
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10CreateDeviceAndSwapChain function


## -description


Create a Direct3D 10.0 device and a swap chain.


## -parameters




### -param pAdapter [in]

Type: <b><a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a>.


### -param DriverType [in]

Type: <b><a href="https://msdn.microsoft.com/0dc66bd9-4e88-460f-a05d-b78347a29cad">D3D10_DRIVER_TYPE</a></b>

The type of driver for the device. See <a href="https://msdn.microsoft.com/0dc66bd9-4e88-460f-a05d-b78347a29cad">D3D10_DRIVER_TYPE</a>.


### -param Software [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMODULE</a></b>

A handle to the DLL that implements a software rasterizer. Must be <b>NULL</b> if DriverType is non-software. The HMODULE of a DLL can be obtained with <a href="http://msdn2.microsoft.com/en-us/library/ms684175.aspx">LoadLibrary</a>, <a href="http://msdn2.microsoft.com/en-us/library/ms684179.aspx">LoadLibraryEx</a>, or <a href="http://msdn2.microsoft.com/en-us/library/ms683199.aspx">GetModuleHandle</a>.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Optional. Device creation flags (see <a href="https://msdn.microsoft.com/4926d630-9748-4416-9af0-287cb06b86f0">D3D10_CREATE_DEVICE_FLAG</a>) that enable <a href="https://msdn.microsoft.com/19c81383-6ac7-49ea-98a3-bf761a32ab40">API layers</a>. These flags can be bitwise OR'd together.


### -param SDKVersion [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Bit flag that indicates the version of the SDK. Should be D3D10_SDK_VERSION, defined in d3d10.h.


### -param pSwapChainDesc [in]

Type: <b><a href="https://msdn.microsoft.com/819d4ff3-f717-46ab-a626-cff065681c79">DXGI_SWAP_CHAIN_DESC</a>*</b>

Description of the swap chain. See <a href="https://msdn.microsoft.com/819d4ff3-f717-46ab-a626-cff065681c79">DXGI_SWAP_CHAIN_DESC</a>.


### -param ppSwapChain [out]

Type: <b><a href="https://msdn.microsoft.com/344ada45-35a0-4e99-b3b7-0f316df029ab">IDXGISwapChain</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/344ada45-35a0-4e99-b3b7-0f316df029ab">IDXGISwapChain</a>.


### -param ppDevice [out]

Type: <b><a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a> that will receive the newly created device.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



To create a device without creating a swap chain, see <a href="https://msdn.microsoft.com/da48d6d4-f35b-4cd1-a358-8eec63dfa674">D3D10CreateDevice</a>.

<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/012577cd-970e-43bc-996e-3be7c2283b60">Core Functions</a>
 

 

