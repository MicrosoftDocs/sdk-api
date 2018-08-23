---
UID: NF:d3d10misc.D3D10CreateDeviceAndSwapChain
title: D3D10CreateDeviceAndSwapChain function
author: windows-sdk-content
description: Create a Direct3D 10.0 device and a swap chain.
old-location: direct3d10\d3d10createdeviceandswapchain.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createdeviceandswapchain.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: D3D10CreateDeviceAndSwapChain, D3D10CreateDeviceAndSwapChain function [Direct3D 10], d3d10misc/D3D10CreateDeviceAndSwapChain, direct3d10.d3d10createdeviceandswapchain, f04f4a8c-494a-567c-ed62-cfe70d6e9474
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d3d10misc.h
req.include-header: 
req.redist: 
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
req.typenames: D3D10_DRIVER_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10CreateDeviceAndSwapChain
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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a>.


### -param DriverType [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205042(v=VS.85).aspx">D3D10_DRIVER_TYPE</a></b>

The type of driver for the device. See <a href="https://msdn.microsoft.com/en-us/library/Bb205042(v=VS.85).aspx">D3D10_DRIVER_TYPE</a>.


### -param Software [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMODULE</a></b>

A handle to the DLL that implements a software rasterizer. Must be <b>NULL</b> if DriverType is non-software. The HMODULE of a DLL can be obtained with <a href="http://msdn2.microsoft.com/en-us/library/ms684175.aspx">LoadLibrary</a>, <a href="http://msdn2.microsoft.com/en-us/library/ms684179.aspx">LoadLibraryEx</a>, or <a href="http://msdn2.microsoft.com/en-us/library/ms683199.aspx">GetModuleHandle</a>.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Optional. Device creation flags (see <a href="https://msdn.microsoft.com/en-us/library/Bb204909(v=VS.85).aspx">D3D10_CREATE_DEVICE_FLAG</a>) that enable <a href="https://msdn.microsoft.com/en-us/library/Bb205068(v=VS.85).aspx">API layers</a>. These flags can be bitwise OR'd together.


### -param SDKVersion [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Bit flag that indicates the version of the SDK. Should be D3D10_SDK_VERSION, defined in d3d10.h.


### -param pSwapChainDesc [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173075(v=VS.85).aspx">DXGI_SWAP_CHAIN_DESC</a>*</b>

Description of the swap chain. See <a href="https://msdn.microsoft.com/en-us/library/Bb173075(v=VS.85).aspx">DXGI_SWAP_CHAIN_DESC</a>.


### -param ppSwapChain [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>.


### -param ppDevice [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a> that will receive the newly created device.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



To create a device without creating a swap chain, see <a href="https://msdn.microsoft.com/en-us/library/Bb205086(v=VS.85).aspx">D3D10CreateDevice</a>.

<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205151(v=VS.85).aspx">Core Functions</a>
 

 

