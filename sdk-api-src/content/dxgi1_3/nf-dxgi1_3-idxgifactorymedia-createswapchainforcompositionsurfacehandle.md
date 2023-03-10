---
UID: NF:dxgi1_3.IDXGIFactoryMedia.CreateSwapChainForCompositionSurfaceHandle
title: IDXGIFactoryMedia::CreateSwapChainForCompositionSurfaceHandle (dxgi1_3.h)
description: Creates a YUV swap chain for an existing DirectComposition surface handle. (IDXGIFactoryMedia.CreateSwapChainForCompositionSurfaceHandle)
helpviewer_keywords: ["CreateSwapChainForCompositionSurfaceHandle","CreateSwapChainForCompositionSurfaceHandle method [DXGI]","CreateSwapChainForCompositionSurfaceHandle method [DXGI]","IDXGIFactoryMedia interface","IDXGIFactoryMedia interface [DXGI]","CreateSwapChainForCompositionSurfaceHandle method","IDXGIFactoryMedia.CreateSwapChainForCompositionSurfaceHandle","IDXGIFactoryMedia::CreateSwapChainForCompositionSurfaceHandle","direct3ddxgi.idxgifactorymedia_createswapchainforcompositionsurfacehandle","dxgi1_3/IDXGIFactoryMedia::CreateSwapChainForCompositionSurfaceHandle"]
old-location: direct3ddxgi\idxgifactorymedia_createswapchainforcompositionsurfacehandle.htm
tech.root: direct3ddxgi
ms.assetid: 3C5724B7-598B-44F1-80F3-07010EAA089B
ms.date: 12/05/2018
ms.keywords: CreateSwapChainForCompositionSurfaceHandle, CreateSwapChainForCompositionSurfaceHandle method [DXGI], CreateSwapChainForCompositionSurfaceHandle method [DXGI],IDXGIFactoryMedia interface, IDXGIFactoryMedia interface [DXGI],CreateSwapChainForCompositionSurfaceHandle method, IDXGIFactoryMedia.CreateSwapChainForCompositionSurfaceHandle, IDXGIFactoryMedia::CreateSwapChainForCompositionSurfaceHandle, direct3ddxgi.idxgifactorymedia_createswapchainforcompositionsurfacehandle, dxgi1_3/IDXGIFactoryMedia::CreateSwapChainForCompositionSurfaceHandle
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDXGIFactoryMedia::CreateSwapChainForCompositionSurfaceHandle
 - dxgi1_3/IDXGIFactoryMedia::CreateSwapChainForCompositionSurfaceHandle
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
 - IDXGIFactoryMedia.CreateSwapChainForCompositionSurfaceHandle
---

# IDXGIFactoryMedia::CreateSwapChainForCompositionSurfaceHandle


## -description

Creates a YUV swap chain for an existing <a href="/windows/desktop/directcomp/reference">DirectComposition</a> surface handle.

## -parameters

### -param pDevice [in]

A pointer to the Direct3D device for the swap chain. This parameter cannot be <b>NULL</b>. Software drivers, like <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE_REFERENCE</a>, are not supported for composition swap chains.

### -param hSurface [in, optional]

A handle to an existing <a href="/windows/desktop/directcomp/reference">DirectComposition</a> surface. This parameter cannot be <b>NULL</b>.

### -param pDesc [in]

A pointer to a  <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a> structure for the swap-chain description. This parameter cannot be <b>NULL</b>.

### -param pRestrictToOutput [in, optional]

A pointer to the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a> interface for the swap chain to restrict content to. If the swap chain is moved to a different output, the content is black. You can optionally set this parameter to an output target that uses <a href="/windows/desktop/direct3ddxgi/dxgi-present">DXGI_PRESENT_RESTRICT_TO_OUTPUT</a> to restrict the content on this output. If the swap chain is moved to a different output, the content is black.

You must also pass the <a href="/windows/desktop/direct3ddxgi/dxgi-present">DXGI_PRESENT_RESTRICT_TO_OUTPUT</a> flag in a present call to force the content to appear blacked out on any other output. If you want to restrict the content to a different output, you must create a new swap chain. However, you can conditionally restrict content based on the <b>DXGI_PRESENT_RESTRICT_TO_OUTPUT</b> flag.

Set this parameter to <b>NULL</b> if you don't want to restrict content to an output target.

### -param ppSwapChain [out]

A pointer to a variable that receives a pointer to the <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a> interface for the swap chain that this method creates.

## -returns

<b>CreateSwapChainForCompositionSurfaceHandle</b> returns:
        <ul>
<li>S_OK if it successfully created a swap chain.</li>
<li>E_OUTOFMEMORY if memory is unavailable to complete the operation.</li>
<li>
<a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a>  if the calling application provided invalid data, for example, if <i>pDesc</i>, <i>pYuvDecodeBuffers</i>, or <i>ppSwapChain</i> is <b>NULL</b>.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic that are defined by the type of device that you pass to <i>pDevice</i>.</li>
</ul>

## -see-also

<a href="/windows/desktop/direct3ddxgi/for-best-performance--use-dxgi-flip-model">For best performance, use DXGI flip model</a>



<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgifactorymedia">IDXGIFactoryMedia</a>
