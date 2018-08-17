---
UID: NF:dxgi.IDXGISwapChain.ResizeBuffers
title: IDXGISwapChain::ResizeBuffers
author: windows-sdk-content
description: Changes the swap chain's back buffer size, format, and number of buffers. This should be called when the application window is resized.
old-location: direct3ddxgi\idxgiswapchain_resizebuffers.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_resizebuffers.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: 615c7678-59c9-07b2-5960-4a5b881f779d, IDXGISwapChain interface [DXGI],ResizeBuffers method, IDXGISwapChain.ResizeBuffers, IDXGISwapChain::ResizeBuffers, ResizeBuffers, ResizeBuffers method [DXGI], ResizeBuffers method [DXGI],IDXGISwapChain interface, direct3ddxgi.idxgiswapchain_resizebuffers, dxgi/IDXGISwapChain::ResizeBuffers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi.h
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
req.typenames: DXGI_SWAP_EFFECT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGISwapChain.ResizeBuffers
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChain::ResizeBuffers


## -description


Changes the swap chain's back buffer size, format, and number of buffers. 
      This should be called when the application window is resized.


## -parameters




### -param BufferCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of buffers in the swap chain (including all back and front buffers). 
            This number can be different from the number of buffers with which you created the swap chain. 
            This number can't be greater than <b>DXGI_MAX_SWAP_CHAIN_BUFFERS</b>. 
            Set this number to zero to preserve the existing number of buffers in the swap chain. 
            You can't specify less than two buffers for the flip presentation model.
          


### -param Width

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The new width of the back buffer. 
            If you specify zero, DXGI will use the width of the client area of the target window. 
            You can't specify the width as zero if you called the <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a> method to create the swap chain for a composition surface.
          


### -param Height

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The new height of the back buffer. 
            If you specify zero, DXGI will use the height of the client area of the target window. 
            You can't specify the height as zero if you called the <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a> method to create the swap chain for a composition surface.
          


### -param NewFormat

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>-typed value for the new format of the back buffer. 
            Set this value to <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT_UNKNOWN</a> to preserve the existing format of the back buffer. 
            The flip presentation model supports a more restricted set of formats than the bit-block transfer (bitblt) model.
          


### -param SwapChainFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/en-us/library/Bb173076(v=VS.85).aspx">DXGI_SWAP_CHAIN_FLAG</a>-typed values that are combined by using a bitwise OR operation. 
            The resulting value specifies options for swap-chain behavior.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; an error code otherwise. 
            For a list of error codes, see <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.
          




## -remarks



You can't resize a swap chain unless you release all outstanding references to its back buffers.
          You must release all of its direct and indirect references on the back buffers in order for <b>ResizeBuffers</b> to succeed.
        

Direct references are held by the application after it calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on a resource.
        

Indirect references are held by views to a resource, binding a view of the resource to a device context,
          a command list that used the resource, a command list that used a view to that resource, a command list that executed another command list that used the
          resource, and so on.
        

Before you call <b>ResizeBuffers</b>, ensure that the application releases all references 
          (by calling the appropriate number of <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> invocations) on the resources, any views to the resource, and any command lists that use either the resources or views, 
          and ensure that neither the resource nor a view is still bound to a device context.
          You can use <a href="https://msdn.microsoft.com/dabf52f5-0f69-4017-863c-9e3ecef4d5dc">ID3D11DeviceContext::ClearState</a> to ensure that all references are released. 
          If a view is bound to a deferred context, you must discard the partially built command list as well (by calling 
          <b>ID3D11DeviceContext::ClearState</b>, then
          <a href="https://msdn.microsoft.com/31e9d8b6-4173-4999-8772-75134d60d269">ID3D11DeviceContext::FinishCommandList</a>, then 
          <b>Release</b> on the command list).
          After you call <b>ResizeBuffers</b>, you can re-query interfaces via <a href="https://msdn.microsoft.com/en-us/library/Bb174570(v=VS.85).aspx">IDXGISwapChain::GetBuffer</a>.
        

For swap chains that you created with <a href="https://msdn.microsoft.com/en-us/library/Bb173076(v=VS.85).aspx">DXGI_SWAP_CHAIN_FLAG_GDI_COMPATIBLE</a>, 
          before you call <b>ResizeBuffers</b>, also call <a href="https://msdn.microsoft.com/2c3a0cf3-c970-4908-a960-ba261756bd5f">IDXGISurface1::ReleaseDC</a> on the swap chain's back-buffer surface 
          to ensure that you have no outstanding GDI device contexts (DCs) open.
        

We recommend that you call <b>ResizeBuffers</b> when a client window is resized (that is, when an application receives a WM_SIZE message).
        

The only difference between <b>IDXGISwapChain::ResizeBuffers</b> in Windows 8 versus Windows 7 is with 
          flip presentation model swap chains that you create with the <a href="https://msdn.microsoft.com/en-us/library/Bb173077(v=VS.85).aspx">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> or DXGI_SWAP_EFFECT_FLIP_DISCARD value set.
          In Windows 8, you must call <b>ResizeBuffers</b> to realize a transition between full-screen mode and windowed mode; 
          otherwise, your next call to the <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">IDXGISwapChain::Present</a> method fails.
        




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>
 

 

