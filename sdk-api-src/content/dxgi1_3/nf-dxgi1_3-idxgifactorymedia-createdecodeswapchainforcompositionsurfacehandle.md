---
UID: NF:dxgi1_3.IDXGIFactoryMedia.CreateDecodeSwapChainForCompositionSurfaceHandle
title: IDXGIFactoryMedia::CreateDecodeSwapChainForCompositionSurfaceHandle (dxgi1_3.h)
description: Creates a YUV swap chain for an existing DirectComposition surface handle. (IDXGIFactoryMedia.CreateDecodeSwapChainForCompositionSurfaceHandle)
helpviewer_keywords: ["CreateDecodeSwapChainForCompositionSurfaceHandle","CreateDecodeSwapChainForCompositionSurfaceHandle method [DXGI]","CreateDecodeSwapChainForCompositionSurfaceHandle method [DXGI]","IDXGIFactoryMedia interface","IDXGIFactoryMedia interface [DXGI]","CreateDecodeSwapChainForCompositionSurfaceHandle method","IDXGIFactoryMedia.CreateDecodeSwapChainForCompositionSurfaceHandle","IDXGIFactoryMedia::CreateDecodeSwapChainForCompositionSurfaceHandle","direct3ddxgi.idxgifactorymedia_createdecodeswapchainforcompositionsurfacehandle","dxgi1_3/IDXGIFactoryMedia::CreateDecodeSwapChainForCompositionSurfaceHandle"]
old-location: direct3ddxgi\idxgifactorymedia_createdecodeswapchainforcompositionsurfacehandle.htm
tech.root: direct3ddxgi
ms.assetid: A4030D6E-EE5A-47E7-A5A2-A008F6869230
ms.date: 12/05/2018
ms.keywords: CreateDecodeSwapChainForCompositionSurfaceHandle, CreateDecodeSwapChainForCompositionSurfaceHandle method [DXGI], CreateDecodeSwapChainForCompositionSurfaceHandle method [DXGI],IDXGIFactoryMedia interface, IDXGIFactoryMedia interface [DXGI],CreateDecodeSwapChainForCompositionSurfaceHandle method, IDXGIFactoryMedia.CreateDecodeSwapChainForCompositionSurfaceHandle, IDXGIFactoryMedia::CreateDecodeSwapChainForCompositionSurfaceHandle, direct3ddxgi.idxgifactorymedia_createdecodeswapchainforcompositionsurfacehandle, dxgi1_3/IDXGIFactoryMedia::CreateDecodeSwapChainForCompositionSurfaceHandle
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
 - IDXGIFactoryMedia::CreateDecodeSwapChainForCompositionSurfaceHandle
 - dxgi1_3/IDXGIFactoryMedia::CreateDecodeSwapChainForCompositionSurfaceHandle
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
 - IDXGIFactoryMedia.CreateDecodeSwapChainForCompositionSurfaceHandle
---

# IDXGIFactoryMedia::CreateDecodeSwapChainForCompositionSurfaceHandle


## -description

Creates a YUV swap chain for an existing <a href="/windows/desktop/directcomp/reference">DirectComposition</a> surface handle.
         The swap chain is created with pre-existing buffers and very few descriptive elements are required. Instead, this method requires 
        a <a href="/windows/desktop/directcomp/reference">DirectComposition</a> surface handle and an <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a> 
        buffer to hold decoded frame data. The swap chain format is determined by the format of the subresources of the <b>IDXGIResource</b>.

## -parameters

### -param pDevice [in]

A pointer to the Direct3D device for the swap chain. This parameter cannot be <b>NULL</b>. 
            Software drivers, like <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE_REFERENCE</a>, are not supported for composition swap chains.

### -param hSurface [in, optional]

A handle to an existing <a href="/windows/desktop/directcomp/reference">DirectComposition</a> surface. This parameter cannot be <b>NULL</b>.

### -param pDesc [in]

A pointer to a  <a href="/windows/desktop/api/dxgi1_3/ns-dxgi1_3-dxgi_decode_swap_chain_desc">DXGI_DECODE_SWAP_CHAIN_DESC</a> structure for the swap-chain description. 
            This parameter cannot be <b>NULL</b>.

### -param pYuvDecodeBuffers [in]

A pointer to a <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a> interface that represents the resource that contains the info 
            that <b>CreateDecodeSwapChainForCompositionSurfaceHandle</b> decodes.

### -param pRestrictToOutput [in, optional]

A pointer to the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a> interface for the swap chain to restrict content to. If the swap chain 
              is moved to a different output, the content is black. You can optionally set this parameter to an output target that 
              uses <a href="/windows/desktop/direct3ddxgi/dxgi-present">DXGI_PRESENT_RESTRICT_TO_OUTPUT</a> to restrict 
              the content on this output. If the swap chain is moved to a different output, the content is black.
            

You must also pass the <a href="/windows/desktop/direct3ddxgi/dxgi-present">DXGI_PRESENT_RESTRICT_TO_OUTPUT</a> flag in a 
              present call to force the content to appear blacked out on any other output. If you want to restrict the content to a different output, you must create a new swap chain. 
              However, you can conditionally restrict content 
              based on the <b>DXGI_PRESENT_RESTRICT_TO_OUTPUT</b> flag.
            

Set this parameter to <b>NULL</b> if you don't want to restrict content to an output target.

### -param ppSwapChain [out]

A pointer to a variable that receives a pointer to the <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidecodeswapchain">IDXGIDecodeSwapChain</a> interface for the 
            swap chain that this method creates.

## -returns

<b>CreateDecodeSwapChainForCompositionSurfaceHandle</b> returns:
              <ul>
<li>S_OK if it successfully created a swap chain.</li>
<li>E_OUTOFMEMORY if memory is unavailable to complete the operation.</li>
<li>
<a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a>  if the calling application provided invalid data, for example, 
                  if <i>pDesc</i>, <i>pYuvDecodeBuffers</i>, or <i>ppSwapChain</i> is <b>NULL</b>.
                </li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic that are defined by the type of
                  device that you pass to <i>pDevice</i>.
                </li>
</ul>

## -remarks

The <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a> provided via the <i>pYuvDecodeBuffers</i> 
      parameter must point to at least one subresource, and all subresources must be created with the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_DECODER</a> flag.

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgifactorymedia">IDXGIFactoryMedia</a>
