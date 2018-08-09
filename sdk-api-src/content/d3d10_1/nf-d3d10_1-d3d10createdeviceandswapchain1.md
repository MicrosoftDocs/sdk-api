---
UID: NF:d3d10_1.D3D10CreateDeviceAndSwapChain1
title: D3D10CreateDeviceAndSwapChain1 function
author: windows-sdk-content
description: Create a Direct3D 10.1 device and a swap chain.
old-location: direct3d10\d3d10createdeviceandswapchain1.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createdeviceandswapchain1.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D3D10CreateDeviceAndSwapChain1, D3D10CreateDeviceAndSwapChain1 function [Direct3D 10], b7c9234e-0746-99a6-b30f-ead0bc077ec3, d3d10_1/D3D10CreateDeviceAndSwapChain1, direct3d10.d3d10createdeviceandswapchain1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d3d10_1.h
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
req.typenames: D3D10_FEATURE_LEVEL1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10_1.dll
api_name:
 - D3D10CreateDeviceAndSwapChain1
product: Windows
targetos: Windows
req.lib: D3D10_1.lib
req.dll: D3D10_1.dll
req.irql: 
---

# D3D10CreateDeviceAndSwapChain1 function


## -description


Create a Direct3D 10.1 device and a swap chain.


## -parameters




### -param pAdapter [in]

Type: <b><a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a>.


### -param DriverType [in]

Type: <b><a href="https://msdn.microsoft.com/0dc66bd9-4e88-460f-a05d-b78347a29cad">D3D10_DRIVER_TYPE</a></b>

The type of driver for the device. See <a href="https://msdn.microsoft.com/0dc66bd9-4e88-460f-a05d-b78347a29cad">D3D10_DRIVER_TYPE</a>.


### -param Software [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMODULE</a></b>

A handle to the DLL that implements a software rasterizer. Must be <b>NULL</b> if DriverType is non-software. 
        The HMODULE of a DLL can be obtained with <a href="http://msdn2.microsoft.com/en-us/library/ms684175.aspx">LoadLibrary</a>, 
          <a href="http://msdn2.microsoft.com/en-us/library/ms684179.aspx">LoadLibraryEx</a>, 
          or <a href="http://msdn2.microsoft.com/en-us/library/ms683199.aspx">GetModuleHandle</a>.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Optional. Device creation flags (see <a href="https://msdn.microsoft.com/4926d630-9748-4416-9af0-287cb06b86f0">D3D10_CREATE_DEVICE_FLAG</a>) that 
        enable <a href="https://msdn.microsoft.com/19c81383-6ac7-49ea-98a3-bf761a32ab40">API layers</a>. These flags can be bitwise OR'd together.


### -param HardwareLevel [in]

Type: <b><a href="https://msdn.microsoft.com/9a6e75ba-3925-4ec7-83c7-53efdcc096cd">D3D10_FEATURE_LEVEL1</a></b>

The version of hardware that is available for acceleration (see <a href="https://msdn.microsoft.com/9a6e75ba-3925-4ec7-83c7-53efdcc096cd">D3D10_FEATURE_LEVEL1</a>).


### -param SDKVersion [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Bit flag that indicates the version of the SDK. Should be D3D10_1_SDK_VERSION, defined in D3D10.h.


### -param pSwapChainDesc [in]

Type: <b><a href="https://msdn.microsoft.com/819d4ff3-f717-46ab-a626-cff065681c79">DXGI_SWAP_CHAIN_DESC</a>*</b>

Description of the swap chain. See <a href="https://msdn.microsoft.com/819d4ff3-f717-46ab-a626-cff065681c79">DXGI_SWAP_CHAIN_DESC</a>.


### -param ppSwapChain [out]

Type: <b><a href="https://msdn.microsoft.com/344ada45-35a0-4e99-b3b7-0f316df029ab">IDXGISwapChain</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/344ada45-35a0-4e99-b3b7-0f316df029ab">IDXGISwapChain</a>.


### -param ppDevice [out]

Type: <b><a href="https://msdn.microsoft.com/511f710d-f35e-46bf-93e0-47b6ceb5c84d">ID3D10Device1</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/511f710d-f35e-46bf-93e0-47b6ceb5c84d">ID3D10Device1 Interface</a> that will receive the newly created device.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



To create a device without creating a swap chain, see <a href="https://msdn.microsoft.com/6eed32f7-985e-4456-815e-d289acba7ae7">D3D10CreateDevice1</a>.

This method requires Windows Vista Service Pack 1, Windows Server 2008, or later release of Windows.

<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/012577cd-970e-43bc-996e-3be7c2283b60">Core Functions</a>
 

 

