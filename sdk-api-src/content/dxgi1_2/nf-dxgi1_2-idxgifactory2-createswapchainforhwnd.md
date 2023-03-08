---
UID: NF:dxgi1_2.IDXGIFactory2.CreateSwapChainForHwnd
title: IDXGIFactory2::CreateSwapChainForHwnd (dxgi1_2.h)
description: Creates a swap chain that is associated with an HWND handle to the output window for the swap chain.
helpviewer_keywords: ["CreateSwapChainForHwnd","CreateSwapChainForHwnd method [DXGI]","CreateSwapChainForHwnd method [DXGI]","IDXGIFactory2 interface","IDXGIFactory2 interface [DXGI]","CreateSwapChainForHwnd method","IDXGIFactory2.CreateSwapChainForHwnd","IDXGIFactory2::CreateSwapChainForHwnd","direct3ddxgi.idxgifactory2_createswapchain1","dxgi1_2/IDXGIFactory2::CreateSwapChainForHwnd"]
old-location: direct3ddxgi\idxgifactory2_createswapchain1.htm
tech.root: direct3ddxgi
ms.assetid: B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD
ms.date: 12/05/2018
ms.keywords: CreateSwapChainForHwnd, CreateSwapChainForHwnd method [DXGI], CreateSwapChainForHwnd method [DXGI],IDXGIFactory2 interface, IDXGIFactory2 interface [DXGI],CreateSwapChainForHwnd method, IDXGIFactory2.CreateSwapChainForHwnd, IDXGIFactory2::CreateSwapChainForHwnd, direct3ddxgi.idxgifactory2_createswapchain1, dxgi1_2/IDXGIFactory2::CreateSwapChainForHwnd
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
 - IDXGIFactory2::CreateSwapChainForHwnd
 - dxgi1_2/IDXGIFactory2::CreateSwapChainForHwnd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIFactory2.CreateSwapChainForHwnd
---

# IDXGIFactory2::CreateSwapChainForHwnd


## -description

Creates a swap chain that is associated with an <a href="/windows/desktop/WinProg/windows-data-types">HWND</a> handle to the output window for the swap chain.

## -parameters

### -param pDevice [in]

For Direct3D 11, and earlier versions of Direct3D, this is a pointer to the Direct3D device for the swap chain. For Direct3D 12 this is a pointer to a direct command queue (refer to <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue">ID3D12CommandQueue</a>). This parameter cannot be <b>NULL</b>.

### -param hWnd [in]

The <a href="/windows/desktop/WinProg/windows-data-types">HWND</a> handle that is associated with the swap chain that <b>CreateSwapChainForHwnd</b> creates. This parameter cannot be <b>NULL</b>.

### -param pDesc [in]

A pointer to a  <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a> structure for the swap-chain description. This parameter cannot be <b>NULL</b>.

### -param pFullscreenDesc [in, optional]

A pointer to a  <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_fullscreen_desc">DXGI_SWAP_CHAIN_FULLSCREEN_DESC</a> structure for the description of a full-screen swap chain. You can optionally set this parameter to create a full-screen swap chain. Set it to <b>NULL</b> to create a windowed swap chain.

### -param pRestrictToOutput [in, optional]

A pointer to the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a> interface for the output to restrict content to. You must also pass the <a href="/windows/desktop/direct3ddxgi/dxgi-present">DXGI_PRESENT_RESTRICT_TO_OUTPUT</a> flag in a <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a> call to force the content to appear blacked out on any other output. If you want to restrict the content to a different output, you must create a new swap chain. However, you can conditionally restrict content based on the <b>DXGI_PRESENT_RESTRICT_TO_OUTPUT</b> flag.


Set this parameter to <b>NULL</b> if you don't want to restrict content to an output target.

### -param ppSwapChain [out]

A pointer to a variable that receives a pointer to the <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a> interface for the swap chain that <b>CreateSwapChainForHwnd</b> creates.

## -returns

<b>CreateSwapChainForHwnd</b> returns:
        <ul>
<li>S_OK if it successfully created a swap chain.</li>
<li>E_OUTOFMEMORY if memory is unavailable to complete the operation.</li>
<li>
<a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a>  if the calling application provided invalid data, for example, if <i>pDesc</i> or <i>ppSwapChain</i> is <b>NULL</b>, or <i>pDesc</i> data members are invalid.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic that are defined by the type of device that you pass to <i>pDevice</i>.</li>
</ul>


<b>Platform Update for Windows 7:  </b><a href="/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_scaling">DXGI_SCALING_NONE</a> is not supported on Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed and causes <b>CreateSwapChainForHwnd</b> to return DXGI_ERROR_INVALID_CALL when called. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -remarks

<div class="alert"><b>Note</b>  Do not use this method in Windows Store apps. Instead, use <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a>.</div>
<div> </div>
If you specify the width, height, or both (<b>Width</b> and <b>Height</b> members of <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a> that <i>pDesc</i> points to) of the swap chain as zero, the runtime obtains the size from the output window that the <i>hWnd</i> parameter specifies.

You can subsequently call the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getdesc1">IDXGISwapChain1::GetDesc1</a> method to retrieve the assigned width or height value.

Because you can associate only one flip presentation model swap chain at a time with an <a href="/windows/desktop/WinProg/windows-data-types">HWND</a>, the Microsoft Direct3D 11 policy of deferring the destruction of objects can cause problems if you attempt to destroy a flip presentation model swap chain and replace it with another swap chain. For more info about this situation, see <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush">Deferred Destruction Issues with Flip Presentation Swap Chains</a>.

For info about how to choose a format for the swap chain's back buffer, see <a href="/windows/desktop/direct3ddxgi/converting-data-color-space">Converting data for the color space</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/for-best-performance--use-dxgi-flip-model">For best performance, use DXGI flip model</a>



<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2">IDXGIFactory2</a>
