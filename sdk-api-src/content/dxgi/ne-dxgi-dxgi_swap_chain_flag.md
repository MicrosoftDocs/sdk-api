---
UID: NE:dxgi.DXGI_SWAP_CHAIN_FLAG
title: DXGI_SWAP_CHAIN_FLAG (dxgi.h)
description: Options for swap-chain behavior.
helpviewer_keywords: ["DXGI_SWAP_CHAIN_FLAG","DXGI_SWAP_CHAIN_FLAG enumeration [DXGI]","DXGI_SWAP_CHAIN_FLAG_ALLOW_MODE_SWITCH","DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING","DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY","DXGI_SWAP_CHAIN_FLAG_FOREGROUND_LAYER","DXGI_SWAP_CHAIN_FLAG_FRAME_LATENCY_WAITABLE_OBJECT","DXGI_SWAP_CHAIN_FLAG_FULLSCREEN_VIDEO","DXGI_SWAP_CHAIN_FLAG_GDI_COMPATIBLE","DXGI_SWAP_CHAIN_FLAG_HW_PROTECTED","DXGI_SWAP_CHAIN_FLAG_NONPREROTATED","DXGI_SWAP_CHAIN_FLAG_RESTRICTED_CONTENT","DXGI_SWAP_CHAIN_FLAG_RESTRICT_SHARED_RESOURCE_DRIVER","DXGI_SWAP_CHAIN_FLAG_YUV_VIDEO","direct3ddxgi.DXGI_SWAP_CHAIN_FLAG","dxgi/DXGI_SWAP_CHAIN_FLAG","dxgi/DXGI_SWAP_CHAIN_FLAG_ALLOW_MODE_SWITCH","dxgi/DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING","dxgi/DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY","dxgi/DXGI_SWAP_CHAIN_FLAG_FOREGROUND_LAYER","dxgi/DXGI_SWAP_CHAIN_FLAG_FRAME_LATENCY_WAITABLE_OBJECT","dxgi/DXGI_SWAP_CHAIN_FLAG_FULLSCREEN_VIDEO","dxgi/DXGI_SWAP_CHAIN_FLAG_GDI_COMPATIBLE","dxgi/DXGI_SWAP_CHAIN_FLAG_HW_PROTECTED","dxgi/DXGI_SWAP_CHAIN_FLAG_NONPREROTATED","dxgi/DXGI_SWAP_CHAIN_FLAG_RESTRICTED_CONTENT","dxgi/DXGI_SWAP_CHAIN_FLAG_RESTRICT_SHARED_RESOURCE_DRIVER","dxgi/DXGI_SWAP_CHAIN_FLAG_YUV_VIDEO","e9b1bfe4-18e3-1a44-ba71-9359f09d8247"]
old-location: direct3ddxgi\DXGI_SWAP_CHAIN_FLAG.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_swap_chain_flag.htm
ms.date: 12/05/2018
ms.keywords: DXGI_SWAP_CHAIN_FLAG, DXGI_SWAP_CHAIN_FLAG enumeration [DXGI], DXGI_SWAP_CHAIN_FLAG_ALLOW_MODE_SWITCH, DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING, DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY, DXGI_SWAP_CHAIN_FLAG_FOREGROUND_LAYER, DXGI_SWAP_CHAIN_FLAG_FRAME_LATENCY_WAITABLE_OBJECT, DXGI_SWAP_CHAIN_FLAG_FULLSCREEN_VIDEO, DXGI_SWAP_CHAIN_FLAG_GDI_COMPATIBLE, DXGI_SWAP_CHAIN_FLAG_HW_PROTECTED, DXGI_SWAP_CHAIN_FLAG_NONPREROTATED, DXGI_SWAP_CHAIN_FLAG_RESTRICTED_CONTENT, DXGI_SWAP_CHAIN_FLAG_RESTRICT_SHARED_RESOURCE_DRIVER, DXGI_SWAP_CHAIN_FLAG_YUV_VIDEO, direct3ddxgi.DXGI_SWAP_CHAIN_FLAG, dxgi/DXGI_SWAP_CHAIN_FLAG, dxgi/DXGI_SWAP_CHAIN_FLAG_ALLOW_MODE_SWITCH, dxgi/DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING, dxgi/DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY, dxgi/DXGI_SWAP_CHAIN_FLAG_FOREGROUND_LAYER, dxgi/DXGI_SWAP_CHAIN_FLAG_FRAME_LATENCY_WAITABLE_OBJECT, dxgi/DXGI_SWAP_CHAIN_FLAG_FULLSCREEN_VIDEO, dxgi/DXGI_SWAP_CHAIN_FLAG_GDI_COMPATIBLE, dxgi/DXGI_SWAP_CHAIN_FLAG_HW_PROTECTED, dxgi/DXGI_SWAP_CHAIN_FLAG_NONPREROTATED, dxgi/DXGI_SWAP_CHAIN_FLAG_RESTRICTED_CONTENT, dxgi/DXGI_SWAP_CHAIN_FLAG_RESTRICT_SHARED_RESOURCE_DRIVER, dxgi/DXGI_SWAP_CHAIN_FLAG_YUV_VIDEO, e9b1bfe4-18e3-1a44-ba71-9359f09d8247
req.header: dxgi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DXGI_SWAP_CHAIN_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_SWAP_CHAIN_FLAG
 - dxgi/DXGI_SWAP_CHAIN_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI.h
api_name:
 - DXGI_SWAP_CHAIN_FLAG
---

## -description

Options for swap-chain behavior.

## -enum-fields

### -field DXGI_SWAP_CHAIN_FLAG_NONPREROTATED:1

Set this flag to turn off automatic image rotation; that is, do not perform a rotation when transferring the contents of the front buffer to the monitor. 
        Use this flag to avoid a bandwidth penalty when an application expects to handle rotation. This option is valid only during full-screen mode.

### -field DXGI_SWAP_CHAIN_FLAG_ALLOW_MODE_SWITCH:2

Set this flag to enable an application to switch modes by calling <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget">IDXGISwapChain::ResizeTarget</a>. 
        When switching from windowed to full-screen mode, the display mode (or monitor resolution) will be changed to match the dimensions of the application window.

### -field DXGI_SWAP_CHAIN_FLAG_GDI_COMPATIBLE:4

Set this flag to enable an application to render using GDI on a swap chain or a surface. 
        This will allow the application to call <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgisurface1-getdc">IDXGISurface1::GetDC</a> on the 0th back buffer or a surface.

This flag is not applicable for Direct3D 12.

### -field DXGI_SWAP_CHAIN_FLAG_RESTRICTED_CONTENT:8

Set this flag to indicate that the swap chain might contain protected content; therefore, the operating system supports the creation of the swap chain only when driver and hardware protection is used.  If the driver and hardware do not support content protection, the call to create a resource for the swap chain fails.

<b>Direct3D 11:  </b>This enumeration value is supported starting with Windows 8.

### -field DXGI_SWAP_CHAIN_FLAG_RESTRICT_SHARED_RESOURCE_DRIVER:16

Set this flag to indicate that shared resources that are created within the swap chain must be protected by using the driver’s mechanism for restricting access to shared surfaces.

<b>Direct3D 11:  </b>This enumeration value is supported starting with Windows 8.

### -field DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY:32

Set this flag to restrict presented content to the local displays. Therefore, the presented content is not accessible via remote accessing or through the <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">desktop duplication APIs</a>.  

This flag supports the window content protection features of Windows. Applications can use this flag to protect their own onscreen window content from being captured or copied through a specific set of public operating system features and APIs.

If you use this flag with windowed (<a href="/windows/desktop/WinProg/windows-data-types">HWND</a> or <b>IWindow</b>) swap chains where another process created the <b>HWND</b>, the owner of the <b>HWND</b> must use the  <a href="/windows/desktop/api/winuser/nf-winuser-setwindowdisplayaffinity">SetWindowDisplayAffinity</a> function appropriately in order to allow calls to <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a> or <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a> to succeed.


<b>Direct3D 11:  </b>This enumeration value is supported starting with Windows 8.

### -field DXGI_SWAP_CHAIN_FLAG_FRAME_LATENCY_WAITABLE_OBJECT:64

Set this flag to create a waitable object you can use to ensure rendering does not begin while a frame is still being presented. When this flag is used, the swapchain's latency must be set with the <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency">IDXGISwapChain2::SetMaximumFrameLatency</a> API instead of <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency">IDXGIDevice1::SetMaximumFrameLatency</a>.

This flag isn't supported in full-screen mode, unless the render API is Direct3D 12.

<b>Note</b>  This enumeration value is supported starting with Windows 8.1.

### -field DXGI_SWAP_CHAIN_FLAG_FOREGROUND_LAYER:128

Set this flag to create a swap chain in the foreground layer for multi-plane rendering. This flag can only be used with <a href="/uwp/api/Windows.UI.Core.CoreWindow">CoreWindow</a> swap chains, which are created with <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">CreateSwapChainForCoreWindow</a>. Apps should not create foreground swap chains if <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgioutput2-supportsoverlays">IDXGIOutput2::SupportsOverlays</a> indicates that hardware support for overlays is not available.

Note that <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers">IDXGISwapChain::ResizeBuffers</a> cannot be used to add or remove this flag.

<b>Note</b>  This enumeration value is supported starting with Windows 8.1.

### -field DXGI_SWAP_CHAIN_FLAG_FULLSCREEN_VIDEO:256

Set this flag to create a swap chain for full-screen video. 

<b>Note</b>  This enumeration value is supported starting with Windows 8.1.

### -field DXGI_SWAP_CHAIN_FLAG_YUV_VIDEO:512

Set this flag to create a swap chain for YUV video.

<b>Note</b>  This enumeration value is supported starting with Windows 8.1.

### -field DXGI_SWAP_CHAIN_FLAG_HW_PROTECTED:1024

Indicates that the swap chain should be created such that all underlying resources can be protected by the hardware.  Resource creation will fail if hardware content protection is not supported.

This flag has the following restrictions:

<ul>
<li>This flag can only be used with swap effect <b>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</b>.</li>
</ul>
<div class="alert"><b>Note</b>  Creating a swap chain using this flag does not automatically guarantee that hardware protection will be enabled for the underlying allocation. Some implementations require that the DRM components are first initialized prior to any guarantees of protection.</div>
<div> </div>
<b>Note</b>  This enumeration value is supported starting with Windows 10.

### -field DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING:2048

Tearing support is a requirement to enable displays that support variable refresh rates to function properly when the application presents a swap chain tied to a full screen borderless window.  Win32 apps can already achieve tearing in fullscreen exclusive mode by calling <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate">SetFullscreenState</a>(TRUE), but the recommended approach for Win32 developers is to use this tearing flag instead. This flag requires the use of a <b>DXGI_SWAP_EFFECT_FLIP_*</b> swap effect.

To check for hardware support of this feature, refer to <a href="/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport">IDXGIFactory5::CheckFeatureSupport</a>. For usage information refer to <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a> and the <a href="/windows/desktop/direct3ddxgi/dxgi-present">DXGI_PRESENT</a> flags.

> [!NOTE]
> [**IDXGISwapChain::ResizeBuffers**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) can't be used to add or remove this flag.

### -field DXGI_SWAP_CHAIN_FLAG_RESTRICTED_TO_ALL_HOLOGRAPHIC_DISPLAYS:4096

## -remarks

This enumeration is used by the <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc">DXGI_SWAP_CHAIN_DESC</a> structure and the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget">IDXGISwapChain::ResizeTarget</a> method.

This enumeration is also used by the  <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a> structure.

You don't need to set <b>DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY</b> for swap chains that you create in full-screen mode  with the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain">IDXGIFactory::CreateSwapChain</a> method because those swap chains already behave as if <b>DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY</b> is set. That is, presented content is not accessible by remote access or through the <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">desktop duplication APIs</a>.

Swap chains that you create with the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, and  <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a> methods are not protected if <b>DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY</b> is not set and are protected if <b>DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY</b> is set. When swap chains are protected, screen scraping is prevented and, in full-screen mode, presented content is not accessible through the <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">desktop duplication APIs</a>.

When you call <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers">IDXGISwapChain::ResizeBuffers</a> to change the swap chain's back buffer, you can reset or change all <b>DXGI_SWAP_CHAIN_FLAG</b> flags.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>
