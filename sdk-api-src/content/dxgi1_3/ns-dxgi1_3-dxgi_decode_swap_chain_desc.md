---
UID: NS:dxgi1_3.DXGI_DECODE_SWAP_CHAIN_DESC
title: DXGI_DECODE_SWAP_CHAIN_DESC (dxgi1_3.h)
description: Used with IDXGIFactoryMedia::CreateDecodeSwapChainForCompositionSurfaceHandle to describe a decode swap chain.
helpviewer_keywords: ["DXGI_DECODE_SWAP_CHAIN_DESC","DXGI_DECODE_SWAP_CHAIN_DESC structure [DXGI]","direct3ddxgi.dxgi_decode_swap_chain_desc","dxgi1_3/DXGI_DECODE_SWAP_CHAIN_DESC"]
old-location: direct3ddxgi\dxgi_decode_swap_chain_desc.htm
tech.root: direct3ddxgi
ms.assetid: 9AAF8E99-E5BC-49B3-8CA6-1F4FC0190B54
ms.date: 12/05/2018
ms.keywords: DXGI_DECODE_SWAP_CHAIN_DESC, DXGI_DECODE_SWAP_CHAIN_DESC structure [DXGI], direct3ddxgi.dxgi_decode_swap_chain_desc, dxgi1_3/DXGI_DECODE_SWAP_CHAIN_DESC
req.header: dxgi1_3.h
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
req.typenames: DXGI_DECODE_SWAP_CHAIN_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_DECODE_SWAP_CHAIN_DESC
 - dxgi1_3/DXGI_DECODE_SWAP_CHAIN_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_3.h
api_name:
 - DXGI_DECODE_SWAP_CHAIN_DESC
---

## -description

Used with [IDXGIFactoryMedia::CreateDecodeSwapChainForCompositionSurfaceHandle](./nf-dxgi1_3-idxgifactorymedia-createdecodeswapchainforcompositionsurfacehandle.md) to describe a decode swap chain.

## -struct-fields

### -field Flags

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT</a></b>

Can be 0, or a combination of **DXGI_SWAP_CHAIN_FLAG_FULLSCREEN_VIDEO** and/or **DXGI_SWAP_CHAIN_FLAG_YUV_VIDEO**. Those named values are members of the <a href="/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_chain_flag">DXGI_SWAP_CHAIN_FLAG</a> enumerated type, and you can combine them by using a bitwise OR operation. The resulting value specifies options for decode swap-chain behavior.

## -see-also

<a href="/windows/win32/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>