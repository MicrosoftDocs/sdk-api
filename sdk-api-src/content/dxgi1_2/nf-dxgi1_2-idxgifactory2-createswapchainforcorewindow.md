---
UID: NF:dxgi1_2.IDXGIFactory2.CreateSwapChainForCoreWindow
title: IDXGIFactory2::CreateSwapChainForCoreWindow (dxgi1_2.h)
description: Creates a swap chain that is associated with the CoreWindow object for the output window for the swap chain.
helpviewer_keywords: ["CreateSwapChainForCoreWindow","CreateSwapChainForCoreWindow method [DXGI]","CreateSwapChainForCoreWindow method [DXGI]","IDXGIFactory2 interface","IDXGIFactory2 interface [DXGI]","CreateSwapChainForCoreWindow method","IDXGIFactory2.CreateSwapChainForCoreWindow","IDXGIFactory2::CreateSwapChainForCoreWindow","direct3ddxgi.idxgifactory2_createswapchainforimmersivewindow","dxgi1_2/IDXGIFactory2::CreateSwapChainForCoreWindow"]
old-location: direct3ddxgi\idxgifactory2_createswapchainforimmersivewindow.htm
tech.root: direct3ddxgi
ms.assetid: B3AC3AEB-3449-4444-9FD3-866A3795C41F
ms.date: 12/05/2018
ms.keywords: CreateSwapChainForCoreWindow, CreateSwapChainForCoreWindow method [DXGI], CreateSwapChainForCoreWindow method [DXGI],IDXGIFactory2 interface, IDXGIFactory2 interface [DXGI],CreateSwapChainForCoreWindow method, IDXGIFactory2.CreateSwapChainForCoreWindow, IDXGIFactory2::CreateSwapChainForCoreWindow, direct3ddxgi.idxgifactory2_createswapchainforimmersivewindow, dxgi1_2/IDXGIFactory2::CreateSwapChainForCoreWindow
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
 - IDXGIFactory2::CreateSwapChainForCoreWindow
 - dxgi1_2/IDXGIFactory2::CreateSwapChainForCoreWindow
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
 - IDXGIFactory2.CreateSwapChainForCoreWindow
---

# IDXGIFactory2::CreateSwapChainForCoreWindow


## -description

Creates a swap chain that is associated with the <a href="/uwp/api/Windows.UI.Core.CoreWindow">CoreWindow</a> object for the output window for the swap chain.

## -parameters

### -param pDevice [in]

For Direct3D 11, and earlier versions of Direct3D, this is a pointer to the Direct3D device for the swap chain. For Direct3D 12 this is a pointer to a direct command queue (refer to <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue">ID3D12CommandQueue</a>). This parameter cannot be <b>NULL</b>.

### -param pWindow [in]

A pointer to the <a href="/uwp/api/Windows.UI.Core.CoreWindow">CoreWindow</a> object that is associated with the swap chain that <b>CreateSwapChainForCoreWindow</b> creates.

### -param pDesc [in]

A pointer to a  <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a> structure for the swap-chain description. This parameter cannot be <b>NULL</b>.

### -param pRestrictToOutput [in, optional]

A pointer to the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a> interface that the swap chain is restricted to. If the swap chain is moved to a different output, the content is black. You can optionally set this parameter to an output target that uses <a href="/windows/desktop/direct3ddxgi/dxgi-present">DXGI_PRESENT_RESTRICT_TO_OUTPUT</a> to restrict the content on this output. If you do not set this parameter to restrict content on an output target, you can set it to <b>NULL</b>.

### -param ppSwapChain [out]

A pointer to a variable that receives a pointer to the <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a> interface for the swap chain that <b>CreateSwapChainForCoreWindow</b> creates.

## -returns

<b>CreateSwapChainForCoreWindow</b> returns:
        <ul>
<li>S_OK if it successfully created a swap chain.</li>
<li>E_OUTOFMEMORY if memory is unavailable to complete the operation.</li>
<li>
<a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a>  if the calling application provided invalid data, for example, if <i>pDesc</i> or <i>ppSwapChain</i> is <b>NULL</b>.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic that are defined by the type of device that you pass to <i>pDevice</i>.</li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>CreateSwapChainForCoreWindow</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -remarks

<div class="alert"><b>Note</b>  Use this method in Windows Store apps rather than <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">IDXGIFactory2::CreateSwapChainForHwnd</a>.</div>
<div> </div>
If you specify the width, height, or both (<b>Width</b> and <b>Height</b> members of <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a> that <i>pDesc</i> points to) of the swap chain as zero, the runtime obtains the size from the output window that the <i>pWindow</i> parameter specifies.

You can subsequently call the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getdesc1">IDXGISwapChain1::GetDesc1</a> method to retrieve the assigned width or height value.

Because you can associate only one flip presentation model swap chain (per layer) at a time with a <a href="/uwp/api/Windows.UI.Core.CoreWindow">CoreWindow</a>, the Microsoft Direct3D 11 policy of deferring the destruction of objects can cause problems if you attempt to destroy a flip presentation model swap chain and replace it with another swap chain. For more info about this situation, see <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush">Deferred Destruction Issues with Flip Presentation Swap Chains</a>.

For info about how to choose a format for the swap chain's back buffer, see <a href="/windows/desktop/direct3ddxgi/converting-data-color-space">Converting data for the color space</a>.

<h3><a id="Overlapping_swap_chains"></a><a id="overlapping_swap_chains"></a><a id="OVERLAPPING_SWAP_CHAINS"></a>Overlapping swap chains</h3>
Starting with Windows 8.1, it is possible to create an additional swap chain in the foreground layer. A foreground swap chain can be used to render UI elements at native resolution while scaling up real-time rendering in the background swap chain (such as gameplay). This enables scenarios where lower resolution rendering is required for faster fill rates, but without sacrificing UI quality.

Foreground swap chains are created by setting the <b>DXGI_SWAP_CHAIN_FLAG_FOREGROUND_LAYER</b> swap chain flag in the <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a> that <i>pDesc</i> points to. Foreground swap chains must also use the <b>DXGI_ALPHA_MODE_PREMULTIPLIED</b> alpha mode, and must use <b>DXGI_SCALING_NONE</b>. Premultiplied alpha means that each pixel's color values are expected to be already multiplied by the alpha value before the frame is presented. For example, a 100% white BGRA pixel at 50% alpha is set to (0.5, 0.5, 0.5, 0.5). The alpha premultiplication step can be done in the output-merger stage by applying an app blend state (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11blendstate">ID3D11BlendState</a>) with the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_render_target_blend_desc">D3D11_RENDER_TARGET_BLEND_DESC</a> structure's <b>SrcBlend</b> field set to <b>D3D11_SRC_ALPHA</b>. If the alpha premultiplication step is not done, colors on the foreground swap chain will be brighter than expected.

The foreground swap chain will use multiplane overlays if supported by the hardware. Call <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgioutput2-supportsoverlays">IDXGIOutput2::SupportsOverlays</a> to query the adapter for overlay support.

The following example creates a foreground swap chain for a CoreWindow:


```cpp

DXGI_SWAP_CHAIN_DESC1 swapChainDesc = { 0 };

swapChainDesc.Width = static_cast<UINT>(m_d3dRenderTargetSize.Width);
swapChainDesc.Height = static_cast<UINT>(m_d3dRenderTargetSize.Height);
swapChainDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
swapChainDesc.Stereo = false;
swapChainDesc.SampleDesc.Count = 1; // Don't use multi-sampling.
swapChainDesc.SampleDesc.Quality = 0;
swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
swapChainDesc.BufferCount = 2;
swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL;
swapChainDesc.Flags = DXGI_SWAP_CHAIN_FLAG_FOREGROUND_LAYER;
swapChainDesc.AlphaMode = DXGI_ALPHA_MODE_PREMULTIPLIED;
swapChainDesc.Scaling = DXGI_SCALING_NONE;

ComPtr<IDXGISwapChain1> swapChain;
HRESULT hr = dxgiFactory->CreateSwapChainForCoreWindow(
    m_d3dDevice.Get(),
    reinterpret_cast<IUnknown*>(m_window.Get()),
    &swapChainDesc,
    nullptr,
    &swapChain
    );
```


Present both swap chains together after rendering is complete.

The following example presents both swap chains:


```cpp

HRESULT hr = m_swapChain->Present(1, 0);

if (SUCCEEDED(hr) && m_foregroundSwapChain)
{
    m_foregroundSwapChain->Present(1, 0);
}
```

## -see-also

<a href="/uwp/api/Windows.UI.Core.CoreWindow">CoreWindow</a>



<a href="/windows/desktop/direct3ddxgi/for-best-performance--use-dxgi-flip-model">For best performance, use DXGI flip model</a>



<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2">IDXGIFactory2</a>