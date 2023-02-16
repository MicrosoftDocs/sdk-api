---
UID: NF:dxgi1_2.IDXGIFactory2.CreateSwapChainForComposition
title: IDXGIFactory2::CreateSwapChainForComposition (dxgi1_2.h)
description: Creates a swap chain that you can use to send Direct3D content into the DirectComposition API or a Xaml framework to compose in a window.
helpviewer_keywords: ["CreateSwapChainForComposition","CreateSwapChainForComposition method [DXGI]","CreateSwapChainForComposition method [DXGI]","IDXGIFactory2 interface","IDXGIFactory2 interface [DXGI]","CreateSwapChainForComposition method","IDXGIFactory2.CreateSwapChainForComposition","IDXGIFactory2::CreateSwapChainForComposition","direct3ddxgi.idxgifactory2_createswapchainforcompositionsurface","dxgi1_2/IDXGIFactory2::CreateSwapChainForComposition"]
old-location: direct3ddxgi\idxgifactory2_createswapchainforcompositionsurface.htm
tech.root: direct3ddxgi
ms.assetid: 8AE13082-F8C3-422A-A111-4E91488BD1AF
ms.date: 08/12/2022
ms.keywords: CreateSwapChainForComposition, CreateSwapChainForComposition method [DXGI], CreateSwapChainForComposition method [DXGI],IDXGIFactory2 interface, IDXGIFactory2 interface [DXGI],CreateSwapChainForComposition method, IDXGIFactory2.CreateSwapChainForComposition, IDXGIFactory2::CreateSwapChainForComposition, direct3ddxgi.idxgifactory2_createswapchainforcompositionsurface, dxgi1_2/IDXGIFactory2::CreateSwapChainForComposition
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
 - IDXGIFactory2::CreateSwapChainForComposition
 - dxgi1_2/IDXGIFactory2::CreateSwapChainForComposition
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
 - IDXGIFactory2.CreateSwapChainForComposition
---

## -description

Creates a swap chain that you can use to send Direct3D content into the <a href="/windows/win32/directcomp/directcomposition-portal">DirectComposition</a> API, to the <a href="/dotnet/api/windows.ui.xaml">Windows.UI.Xaml</a> framework, or to [Windows UI Library (WinUI)](https://docs.microsoft.com/windows/apps/winui/) XAML, to compose in a window.

## -parameters

### -param pDevice [in]

For Direct3D 11, and earlier versions of Direct3D, this is a pointer to the Direct3D device for the swap chain. For Direct3D 12 this is a pointer to a direct command queue (refer to <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue">ID3D12CommandQueue</a>). This parameter cannot be <b>NULL</b>. Software drivers, like <a href="/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE_REFERENCE</a>, are not supported for composition swap chains.

### -param pDesc [in]

A pointer to a  <a href="/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a> structure for the swap-chain description. This parameter cannot be <b>NULL</b>.

You must specify the <a href="/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> value in the <b>SwapEffect</b> member of <a href="/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a> because <b>CreateSwapChainForComposition</b> supports only <a href="/windows/win32/direct3ddxgi/dxgi-flip-model">flip presentation model</a>.

You must also specify the <a href="/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_scaling">DXGI_SCALING_STRETCH</a> value in the <b>Scaling</b> member of <a href="/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a>.

### -param pRestrictToOutput [in, optional]

A pointer to the <a href="/windows/win32/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a> interface for the output to restrict content to. You must also pass the <a href="/windows/win32/direct3ddxgi/dxgi-present">DXGI_PRESENT_RESTRICT_TO_OUTPUT</a> flag in a <a href="/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a> call to force the content to appear blacked out on any other output. If you want to restrict the content to a different output, you must create a new swap chain. However, you can conditionally restrict content based on the <b>DXGI_PRESENT_RESTRICT_TO_OUTPUT</b> flag.

Set this parameter to <b>NULL</b> if you don't want to restrict content to an output target.

### -param ppSwapChain [out]

A pointer to a variable that receives a pointer to the <a href="/windows/win32/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a> interface for the swap chain that <b>CreateSwapChainForComposition</b> creates.

## -returns

<b>CreateSwapChainForComposition</b> returns:
        <ul>
<li>S_OK if it successfully created a swap chain.</li>
<li>E_OUTOFMEMORY if memory is unavailable to complete the operation.</li>
<li>
<a href="/windows/win32/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a>  if the calling application provided invalid data, for example, if <i>pDesc</i> or <i>ppSwapChain</i> is <b>NULL</b>.</li>
<li>Possibly other error codes that are described in the <a href="/windows/win32/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic that are defined by the type of device that you pass to <i>pDevice</i>.</li>
</ul>

<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>CreateSwapChainForComposition</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="/windows/win32/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -remarks

You can use composition swap chains with either:

* <a href="/windows/win32/directcomp/directcomposition-portal">DirectComposition</a>'s <a href="/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a> interface,
* System XAML's [SwapChainPanel](/uwp/api/windows.ui.xaml.controls.swapchainpanel) or [SwapChainBackgroundPanel](/uwp/api/windows.ui.xaml.controls.swapchainbackgroundpanel) classes.
* [Windows UI Library (WinUI) 3](https://docs.microsoft.com/windows/apps/winui/) XAML's [SwapChainPanel](/windows/windows-app-sdk/api/winrt/microsoft.ui.xaml.controls.swapchainpanel) or [SwapChainBackgroundPanel](/windows/windows-app-sdk/api/winrt/microsoft.ui.xaml.controls.swapchainbackgroundpanel) classes.

For DirectComposition, you can call the <a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent">IDCompositionVisual::SetContent</a> method to set the swap chain as the content of a <a href="/windows/win32/directcomp/basic-concepts">visual object</a>, which then allows you to bind the swap chain to the visual tree. For XAML, the <b>SwapChainBackgroundPanel</b> class exposes a classic COM interface <b>ISwapChainBackgroundPanelNative</b>. You can use the <a href="/windows/win32/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-iswapchainbackgroundpanelnative-setswapchain">ISwapChainBackgroundPanelNative::SetSwapChain</a> method to bind to the XAML UI graph. For info about how to use composition swap chains with XAML’s <b>SwapChainBackgroundPanel</b> class, see <a href="/windows/uwp/gaming/directx-and-xaml-interop">DirectX and XAML interop</a>.

The <a href="/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate">IDXGISwapChain::SetFullscreenState</a>, <a href="/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget">IDXGISwapChain::ResizeTarget</a>, <a href="/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput">IDXGISwapChain::GetContainingOutput</a>, <a href="/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-gethwnd">IDXGISwapChain1::GetHwnd</a>, and <a href="/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow">IDXGISwapChain::GetCoreWindow</a> methods aren't valid on this type of swap chain. If you call any of these methods on this type of swap chain, they fail.

For info about how to choose a format for the swap chain's back buffer, see <a href="/windows/win32/direct3ddxgi/converting-data-color-space">Converting data for the color space</a>.

## Examples

For a code example showing how to use <b>CreateSwapChainForComposition</b>, see [SwapChainPanel and gaming](/windows/uwp/gaming/directx-and-xaml-interop#swapchainpanel-and-gaming).

* For WinRT XAML, the [ISwapChainPanelNative](/windows/win32/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative) and [ISwapChainBackgroundPanelNative](/windows/win32/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainbackgroundpanelnative) interfaces are declared in the `windows.ui.xaml.media.dxinterop.h` header.
* For [Windows UI Library (WinUI)](https://docs.microsoft.com/windows/apps/winui/) XAML, the **ISwapChainPanelNative** and **ISwapChainBackgroundPanelNative** interfaces are declared in the `microsoft.ui.xaml.media.dxinterop.h` header.

## -see-also

* <a href="/windows/win32/direct3ddxgi/for-best-performance--use-dxgi-flip-model">For best performance, use DXGI flip model</a>
* <a href="/windows/win32/api/dxgi1_2/nn-dxgi1_2-idxgifactory2">IDXGIFactory2</a>
