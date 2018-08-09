---
UID: NE:dxgi.DXGI_SWAP_CHAIN_FLAG
title: DXGI_SWAP_CHAIN_FLAG
author: windows-sdk-content
description: Options for swap-chain behavior.
old-location: direct3ddxgi\DXGI_SWAP_CHAIN_FLAG.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_swap_chain_flag.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DXGI_SWAP_CHAIN_FLAG, DXGI_SWAP_CHAIN_FLAG enumeration [DXGI], DXGI_SWAP_CHAIN_FLAG_ALLOW_MODE_SWITCH, DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING, DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY, DXGI_SWAP_CHAIN_FLAG_FOREGROUND_LAYER, DXGI_SWAP_CHAIN_FLAG_FRAME_LATENCY_WAITABLE_OBJECT, DXGI_SWAP_CHAIN_FLAG_FULLSCREEN_VIDEO, DXGI_SWAP_CHAIN_FLAG_GDI_COMPATIBLE, DXGI_SWAP_CHAIN_FLAG_HW_PROTECTED, DXGI_SWAP_CHAIN_FLAG_NONPREROTATED, DXGI_SWAP_CHAIN_FLAG_RESTRICTED_CONTENT, DXGI_SWAP_CHAIN_FLAG_RESTRICT_SHARED_RESOURCE_DRIVER, DXGI_SWAP_CHAIN_FLAG_YUV_VIDEO, direct3ddxgi.DXGI_SWAP_CHAIN_FLAG, dxgi/DXGI_SWAP_CHAIN_FLAG, dxgi/DXGI_SWAP_CHAIN_FLAG_ALLOW_MODE_SWITCH, dxgi/DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING, dxgi/DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY, dxgi/DXGI_SWAP_CHAIN_FLAG_FOREGROUND_LAYER, dxgi/DXGI_SWAP_CHAIN_FLAG_FRAME_LATENCY_WAITABLE_OBJECT, dxgi/DXGI_SWAP_CHAIN_FLAG_FULLSCREEN_VIDEO, dxgi/DXGI_SWAP_CHAIN_FLAG_GDI_COMPATIBLE, dxgi/DXGI_SWAP_CHAIN_FLAG_HW_PROTECTED, dxgi/DXGI_SWAP_CHAIN_FLAG_NONPREROTATED, dxgi/DXGI_SWAP_CHAIN_FLAG_RESTRICTED_CONTENT, dxgi/DXGI_SWAP_CHAIN_FLAG_RESTRICT_SHARED_RESOURCE_DRIVER, dxgi/DXGI_SWAP_CHAIN_FLAG_YUV_VIDEO, e9b1bfe4-18e3-1a44-ba71-9359f09d8247
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: DXGI_SWAP_CHAIN_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI.h
api_name:
 - DXGI_SWAP_CHAIN_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_SWAP_CHAIN_FLAG enumeration


## -description


Options for swap-chain behavior.


## -enum-fields




### -field DXGI_SWAP_CHAIN_FLAG_NONPREROTATED

Set this flag to turn off automatic image rotation; that is, do not perform a rotation when transferring the contents of the front buffer to the monitor. 
        Use this flag to avoid a bandwidth penalty when an application expects to handle rotation. This option is valid only during full-screen mode. 


### -field DXGI_SWAP_CHAIN_FLAG_ALLOW_MODE_SWITCH

Set this flag to enable an application to switch modes by calling <a href="https://msdn.microsoft.com/en-us/library/Bb174578(v=VS.85).aspx">IDXGISwapChain::ResizeTarget</a>. 
        When switching from windowed to full-screen mode, the display mode (or monitor resolution) will be changed to match the dimensions of the application window.


### -field DXGI_SWAP_CHAIN_FLAG_GDI_COMPATIBLE

Set this flag to enable an application to render using GDI on a swap chain or a surface. 
        This will allow the application to call <a href="https://msdn.microsoft.com/b148d2b4-36a2-46b9-8a98-9f3c478549a4">IDXGISurface1::GetDC</a> on the 0th back buffer or a surface.


### -field DXGI_SWAP_CHAIN_FLAG_RESTRICTED_CONTENT

Set this flag to indicate that the swap chain might contain protected content; therefore, the operating system supports the creation of the swap chain only when driver and hardware protection is used.  If the driver and hardware do not support content protection, the call to create a resource for the swap chain fails.

<b>Direct3D 11:  </b>This enumeration value is supported starting with Windows 8.


### -field DXGI_SWAP_CHAIN_FLAG_RESTRICT_SHARED_RESOURCE_DRIVER

Set this flag to indicate that shared resources that are created within the swap chain must be protected by using the driver’s mechanism for restricting access to shared surfaces.

<b>Direct3D 11:  </b>This enumeration value is supported starting with Windows 8.


### -field DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY

Set this flag to restrict presented content to the local displays. Therefore, the presented content is not accessible via remote accessing or through the <a href="https://msdn.microsoft.com/02C4EC3D-D97F-4CFC-ABF5-03B44CE6A658">desktop duplication APIs</a>.  

This flag supports the window content protection features of Windows. Applications can use this flag to protect their own onscreen window content from being captured or copied through a specific set of public operating system features and APIs.

If you use this flag with windowed (<a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a> or <b>IWindow</b>) swap chains where another process created the <b>HWND</b>, the owner of the <b>HWND</b> must use the  <a href="https://msdn.microsoft.com/en-us/library/Dd375340(v=VS.85).aspx">SetWindowDisplayAffinity</a> function appropriately in order to allow calls to <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">IDXGISwapChain::Present</a> or <a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">IDXGISwapChain1::Present1</a> to succeed.


<b>Direct3D 11:  </b>This enumeration value is supported starting with Windows 8.


### -field DXGI_SWAP_CHAIN_FLAG_FRAME_LATENCY_WAITABLE_OBJECT

Set this flag to create a waitable object you can use to ensure rendering does not begin while a frame is still being presented. When this flag is used, the swapchain's latency must be set with the <a href="https://msdn.microsoft.com/AF3F03F2-38B4-474A-8A66-86A93D776EA0">IDXGISwapChain2::SetMaximumFrameLatency</a> API instead of <a href="https://msdn.microsoft.com/ea477f33-2dba-44ac-9b47-8fd2ce6cec30">IDXGIDevice1::SetMaximumFrameLatency</a>.

<b>Note</b>  This enumeration value is supported starting with Windows 8.1.


### -field DXGI_SWAP_CHAIN_FLAG_FOREGROUND_LAYER

Set this flag to create a swap chain in the foreground layer for multi-plane rendering. This flag can only be used with <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> swap chains, which are created with <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">CreateSwapChainForCoreWindow</a>. Apps should not create foreground swap chains if <a href="https://msdn.microsoft.com/BC9CD287-CD89-4D0C-ADE3-EAA60D5FEAAD">IDXGIOutput2::SupportsOverlays</a> indicates that hardware support for overlays is not available.

Note that <a href="https://msdn.microsoft.com/en-us/library/Bb174577(v=VS.85).aspx">IDXGISwapChain::ResizeBuffers</a> cannot be used to add or remove this flag.

<b>Note</b>  This enumeration value is supported starting with Windows 8.1.


### -field DXGI_SWAP_CHAIN_FLAG_FULLSCREEN_VIDEO

Set this flag to create a swap chain for full-screen video. 

<b>Note</b>  This enumeration value is supported starting with Windows 8.1.


### -field DXGI_SWAP_CHAIN_FLAG_YUV_VIDEO

Set this flag to create a swap chain for YUV video.

<b>Note</b>  This enumeration value is supported starting with Windows 8.1.


### -field DXGI_SWAP_CHAIN_FLAG_HW_PROTECTED

Indicates that the swap chain should be created such that all underlying resources can be protected by the hardware.  Resource creation will fail if hardware content protection is not supported.

This flag has the following restrictions:

<ul>
<li>This flag can only be used with swap effect <b>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</b>.</li>
</ul>
<div class="alert"><b>Note</b>  Creating a swap chain using this flag does not automatically guarantee that hardware protection will be enabled for the underlying allocation. Some implementations require that the DRM components are first initialized prior to any guarantees of protection.</div>
<div> </div>
<b>Note</b>  This enumeration value is supported starting with Windows 10.


### -field DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING

Tearing support is a requirement to enable displays that support variable refresh rates to function properly when the application presents a swap chain tied to a full screen borderless window.  Win32 apps can already achieve tearing in fullscreen exclusive mode by calling <a href="https://msdn.microsoft.com/en-us/library/Bb174579(v=VS.85).aspx">SetFullscreenState</a>(TRUE), but the recommended approach for Win32 developers is to use this tearing flag instead. This flag requires the use of a <b>DXGI_SWAP_EFFECT_FLIP_*</b> swap effect.

To check for hardware support of this feature, refer to <a href="https://msdn.microsoft.com/959F83F8-ADC6-4609-8F63-BEDDFC2EF088">IDXGIFactory5::CheckFeatureSupport</a>. For usage information refer to <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">IDXGISwapChain::Present</a> and the <a href="https://msdn.microsoft.com/en-us/library/Bb509554(v=VS.85).aspx">DXGI_PRESENT</a> flags.


### -field DXGI_SWAP_CHAIN_FLAG_RESTRICTED_TO_ALL_HOLOGRAPHIC_DISPLAYS




## -remarks



This enumeration is used by the <a href="https://msdn.microsoft.com/en-us/library/Bb173075(v=VS.85).aspx">DXGI_SWAP_CHAIN_DESC</a> structure and the <a href="https://msdn.microsoft.com/en-us/library/Bb174578(v=VS.85).aspx">IDXGISwapChain::ResizeTarget</a> method.

This enumeration is also used by the  <a href="https://msdn.microsoft.com/38B302DF-5617-4195-8E4A-619D75188AD5">DXGI_SWAP_CHAIN_DESC1</a> structure.

You don't need to set <b>DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY</b> for swap chains that you create in full-screen mode  with the <a href="https://msdn.microsoft.com/en-us/library/Bb174537(v=VS.85).aspx">IDXGIFactory::CreateSwapChain</a> method because those swap chains already behave as if <b>DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY</b> is set. That is, presented content is not accessible by remote access or through the <a href="https://msdn.microsoft.com/02C4EC3D-D97F-4CFC-ABF5-03B44CE6A658">desktop duplication APIs</a>.

Swap chains that you create with the <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, and  <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a> methods are not protected if <b>DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY</b> is not set and are protected if <b>DXGI_SWAP_CHAIN_FLAG_DISPLAY_ONLY</b> is set. When swap chains are protected, screen scraping is prevented and, in full-screen mode, presented content is not accessible through the <a href="https://msdn.microsoft.com/02C4EC3D-D97F-4CFC-ABF5-03B44CE6A658">desktop duplication APIs</a>.

When you call <a href="https://msdn.microsoft.com/en-us/library/Bb174577(v=VS.85).aspx">IDXGISwapChain::ResizeBuffers</a> to change the swap chain's back buffer, you can reset or change all <b>DXGI_SWAP_CHAIN_FLAG</b> flags.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

