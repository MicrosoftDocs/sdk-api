---
UID: NS:dxgi1_2.DXGI_SWAP_CHAIN_FULLSCREEN_DESC
title: DXGI_SWAP_CHAIN_FULLSCREEN_DESC (dxgi1_2.h)
description: Describes full-screen mode for a swap chain.
helpviewer_keywords: ["DXGI_SWAP_CHAIN_FULLSCREEN_DESC","DXGI_SWAP_CHAIN_FULLSCREEN_DESC structure [DXGI]","direct3ddxgi.dxgi_swap_chain_fullscreen_desc","dxgi1_2/DXGI_SWAP_CHAIN_FULLSCREEN_DESC"]
old-location: direct3ddxgi\dxgi_swap_chain_fullscreen_desc.htm
tech.root: direct3ddxgi
ms.assetid: 0EE5683E-0623-4FD7-A77F-B64F90A25C6A
ms.date: 12/05/2018
ms.keywords: DXGI_SWAP_CHAIN_FULLSCREEN_DESC, DXGI_SWAP_CHAIN_FULLSCREEN_DESC structure [DXGI], direct3ddxgi.dxgi_swap_chain_fullscreen_desc, dxgi1_2/DXGI_SWAP_CHAIN_FULLSCREEN_DESC
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DXGI_SWAP_CHAIN_FULLSCREEN_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_SWAP_CHAIN_FULLSCREEN_DESC
 - dxgi1_2/DXGI_SWAP_CHAIN_FULLSCREEN_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_2.h
api_name:
 - DXGI_SWAP_CHAIN_FULLSCREEN_DESC
---

# DXGI_SWAP_CHAIN_FULLSCREEN_DESC structure


## -description

Describes full-screen mode for a swap chain.

## -struct-fields

### -field RefreshRate

A <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational">DXGI_RATIONAL</a> structure that describes the refresh rate in hertz. Setting the numerator to 0 forces the native display's refresh rate.

### -field ScanlineOrdering

A member of the <a href="/previous-versions/windows/desktop/legacy/bb173067(v=vs.85)">DXGI_MODE_SCANLINE_ORDER</a> enumerated type that describes the scan-line drawing mode.

### -field Scaling

A member of the <a href="/previous-versions/windows/desktop/legacy/bb173066(v=vs.85)">DXGI_MODE_SCALING</a> enumerated type that describes the scaling mode.

### -field Windowed

A Boolean value that specifies whether the swap chain is in windowed mode. <b>TRUE</b> if the swap chain is in windowed mode; otherwise, <b>FALSE</b>.

## -remarks

This structure is used by the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">CreateSwapChainForHwnd</a> and <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getfullscreendesc">GetFullscreenDesc</a> methods.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>
