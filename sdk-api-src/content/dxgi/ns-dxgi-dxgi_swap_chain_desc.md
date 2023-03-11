---
UID: NS:dxgi.DXGI_SWAP_CHAIN_DESC
title: DXGI_SWAP_CHAIN_DESC (dxgi.h)
description: Describes a swap chain. (DXGI_SWAP_CHAIN_DESC)
helpviewer_keywords: ["04b5d6e7-f014-9f92-ee14-6dd943b40ce5","DXGI_SWAP_CHAIN_DESC","DXGI_SWAP_CHAIN_DESC structure [DXGI]","direct3ddxgi.dxgi_swap_chain_desc","dxgi/DXGI_SWAP_CHAIN_DESC"]
old-location: direct3ddxgi\dxgi_swap_chain_desc.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_swap_chain_desc.htm
ms.date: 12/05/2018
ms.keywords: 04b5d6e7-f014-9f92-ee14-6dd943b40ce5, DXGI_SWAP_CHAIN_DESC, DXGI_SWAP_CHAIN_DESC structure [DXGI], direct3ddxgi.dxgi_swap_chain_desc, dxgi/DXGI_SWAP_CHAIN_DESC
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
req.typenames: DXGI_SWAP_CHAIN_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_SWAP_CHAIN_DESC
 - dxgi/DXGI_SWAP_CHAIN_DESC
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
 - DXGI_SWAP_CHAIN_DESC
---

# DXGI_SWAP_CHAIN_DESC structure


## -description

Describes a swap chain.

## -struct-fields

### -field BufferDesc

Type: <b><a href="/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)">DXGI_MODE_DESC</a></b>

A <a href="/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)">DXGI_MODE_DESC</a> structure that describes the backbuffer display mode.

### -field SampleDesc

Type: <b><a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc">DXGI_SAMPLE_DESC</a></b>

A <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc">DXGI_SAMPLE_DESC</a> structure that describes multi-sampling parameters.

### -field BufferUsage

Type: <b><a href="/windows/desktop/direct3ddxgi/dxgi-usage">DXGI_USAGE</a></b>

A member of the <a href="/windows/desktop/direct3ddxgi/dxgi-usage">DXGI_USAGE</a> enumerated type that describes the surface usage and CPU access options for the back buffer. The back buffer can 
        be used for shader input or render-target output.

### -field BufferCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value that describes the number of buffers in the swap chain. When you call  <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain">IDXGIFactory::CreateSwapChain</a> to create a full-screen swap chain, you typically include the front buffer in this value. For more information about swap-chain buffers, see Remarks.

### -field OutputWindow

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

An <a href="/windows/desktop/WinProg/windows-data-types">HWND</a> handle to the output window. This member must not be <b>NULL</b>.

### -field Windowed

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

A Boolean value that specifies whether the output is in windowed mode. <b>TRUE</b> if the output is in windowed mode; otherwise, <b>FALSE</b>. 

We recommend that you create a windowed swap chain and allow the end user to change the swap chain to full screen through <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate">IDXGISwapChain::SetFullscreenState</a>; that is, do not set this member to FALSE to force the swap chain to be full screen. However, if you create the swap chain as full screen, also provide the end user with a list of supported display modes through the <b>BufferDesc</b> member because a swap chain that is created with an unsupported display mode might cause the display to go black and prevent the end user from seeing anything. 

For more information about choosing windowed verses full screen, see <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain">IDXGIFactory::CreateSwapChain</a>.

### -field SwapEffect

Type: <b><a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT</a></b>

A member of the <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT</a> enumerated type that describes options for handling the contents of the presentation buffer after 
        presenting a surface.

### -field Flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A member of the <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag">DXGI_SWAP_CHAIN_FLAG</a> enumerated type that describes options for swap-chain behavior.

## -remarks

This structure is used by the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getdesc">GetDesc</a> and <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain">CreateSwapChain</a> methods.

In full-screen mode, there is a dedicated front buffer; in windowed mode, the desktop is the front buffer.

If you create a swap chain with one buffer, specifying <b>DXGI_SWAP_EFFECT_SEQUENTIAL</b> does not cause the contents of the single 
      buffer to be swapped with the front buffer.

For performance information about flipping swap-chain buffers in full-screen application, 
      see <a href="/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi">Full-Screen Application Performance Hints</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>



<a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain">IDXGIFactory::CreateSwapChain</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>
