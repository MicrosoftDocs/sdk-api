---
UID: NF:dxgi1_2.IDXGISwapChain1.SetBackgroundColor
title: IDXGISwapChain1::SetBackgroundColor (dxgi1_2.h)
description: Changes the background color of the swap chain.
helpviewer_keywords: ["IDXGISwapChain1 interface [DXGI]","SetBackgroundColor method","IDXGISwapChain1.SetBackgroundColor","IDXGISwapChain1::SetBackgroundColor","SetBackgroundColor","SetBackgroundColor method [DXGI]","SetBackgroundColor method [DXGI]","IDXGISwapChain1 interface","direct3ddxgi.idxgiswapchain1_setbackgroundcolor","dxgi1_2/IDXGISwapChain1::SetBackgroundColor"]
old-location: direct3ddxgi\idxgiswapchain1_setbackgroundcolor.htm
tech.root: direct3ddxgi
ms.assetid: E46CA219-303F-40D4-8C62-6241C9199BA0
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain1 interface [DXGI],SetBackgroundColor method, IDXGISwapChain1.SetBackgroundColor, IDXGISwapChain1::SetBackgroundColor, SetBackgroundColor, SetBackgroundColor method [DXGI], SetBackgroundColor method [DXGI],IDXGISwapChain1 interface, direct3ddxgi.idxgiswapchain1_setbackgroundcolor, dxgi1_2/IDXGISwapChain1::SetBackgroundColor
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDXGISwapChain1::SetBackgroundColor
 - dxgi1_2/IDXGISwapChain1::SetBackgroundColor
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
 - IDXGISwapChain1.SetBackgroundColor
---

# IDXGISwapChain1::SetBackgroundColor


## -description

Changes the background color of the swap chain.

## -parameters

### -param pColor [in]

A pointer to a <a href="/windows/desktop/direct3ddxgi/dxgi-rgba">DXGI_RGBA</a> structure that specifies the background color to set.

## -returns

<b>SetBackgroundColor</b> returns:
        <ul>
<li>S_OK if it successfully set the background color.</li>
<li>E_INVALIDARG if the <i>pColor</i> parameter is incorrect, for example, <i>pColor</i> is NULL or any of the floating-point values of the members of <a href="/windows/desktop/direct3ddxgi/dxgi-rgba">DXGI_RGBA</a> to which <i>pColor</i> points are outside the range from 0.0 through 1.0.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>SetBackgroundColor</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -remarks

The background color affects only swap chains that you create with <a href="/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_scaling">DXGI_SCALING_NONE</a> in windowed mode. You pass this value in a call to <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, or  <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a>. Typically, the background color is not visible unless the swap-chain contents are smaller than the destination window.

When you set the background color, it is not immediately realized. It takes effect in conjunction with your next call to the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a> method. The <a href="/windows/desktop/direct3ddxgi/dxgi-present">DXGI_PRESENT</a> flags that you pass to <b>IDXGISwapChain1::Present1</b> can help achieve the effect that you require. For example, if you call <b>SetBackgroundColor</b> and then call <b>IDXGISwapChain1::Present1</b> with the <i>Flags</i> parameter set to <a href="/windows/desktop/direct3ddxgi/dxgi-present">DXGI_PRESENT_DO_NOT_SEQUENCE</a>, you change only the background color without changing the displayed contents of the swap chain.

When you call the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a> method to display contents of the swap chain, <b>IDXGISwapChain1::Present1</b> uses the <a href="/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode">DXGI_ALPHA_MODE</a> value that is specified in the <b>AlphaMode</b> member of the <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a> structure to determine how to handle the <b>a</b> member of the <a href="/windows/desktop/direct3ddxgi/dxgi-rgba">DXGI_RGBA</a> structure, the alpha value of the background color, that achieves window transparency. For example, if <b>AlphaMode</b> is <b>DXGI_ALPHA_MODE_IGNORE</b>, <b>IDXGISwapChain1::Present1</b> ignores the a member of <b>DXGI_RGBA</b>.

<div class="alert"><b>Note</b>  Like all presentation data, we recommend that you perform floating point operations in a linear color space. When the desktop is in a fixed bit color depth mode, the operating system converts linear color data to standard RGB data (sRGB, gamma 2.2 corrected space) to compose to the screen. For more info, see <a href="/windows/desktop/direct3ddxgi/converting-data-color-space">Converting data for the color space</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_scaling">DXGI_SCALING</a>



<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a>



<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor">IDXGISwapChain1::GetBackgroundColor</a>