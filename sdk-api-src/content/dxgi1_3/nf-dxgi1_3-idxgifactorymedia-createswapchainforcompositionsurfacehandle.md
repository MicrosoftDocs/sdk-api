---
UID: NF:dxgi1_3.IDXGIFactoryMedia.CreateSwapChainForCompositionSurfaceHandle
title: IDXGIFactoryMedia::CreateSwapChainForCompositionSurfaceHandle
author: windows-sdk-content
description: Creates a YUV swap chain for an existing DirectComposition surface handle.
old-location: direct3ddxgi\idxgifactorymedia_createswapchainforcompositionsurfacehandle.htm
tech.root: direct3ddxgi
ms.assetid: 3C5724B7-598B-44F1-80F3-07010EAA089B
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CreateSwapChainForCompositionSurfaceHandle, CreateSwapChainForCompositionSurfaceHandle method [DXGI], CreateSwapChainForCompositionSurfaceHandle method [DXGI],IDXGIFactoryMedia interface, IDXGIFactoryMedia interface [DXGI],CreateSwapChainForCompositionSurfaceHandle method, IDXGIFactoryMedia.CreateSwapChainForCompositionSurfaceHandle, IDXGIFactoryMedia::CreateSwapChainForCompositionSurfaceHandle, direct3ddxgi.idxgifactorymedia_createswapchainforcompositionsurfacehandle, dxgi1_3/IDXGIFactoryMedia::CreateSwapChainForCompositionSurfaceHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIFactoryMedia::CreateSwapChainForCompositionSurfaceHandle


## -description


Creates a YUV swap chain for an existing <a href="https://msdn.microsoft.com/A220189D-8546-4352-8F6F-AC5D2192940D">DirectComposition</a> surface handle.


## -parameters




### -param pDevice [in]

A pointer to the Direct3D device for the swap chain. This parameter cannot be <b>NULL</b>. Software drivers, like <a href="https://msdn.microsoft.com/ceeec7d6-4bdc-488c-80a8-6c5e11986d6a">D3D_DRIVER_TYPE_REFERENCE</a>, are not supported for composition swap chains.


### -param hSurface [in, optional]

A handle to an existing <a href="https://msdn.microsoft.com/A220189D-8546-4352-8F6F-AC5D2192940D">DirectComposition</a> surface. This parameter cannot be <b>NULL</b>.


### -param pDesc [in]

A pointer to a  <a href="https://msdn.microsoft.com/38B302DF-5617-4195-8E4A-619D75188AD5">DXGI_SWAP_CHAIN_DESC1</a> structure for the swap-chain description. This parameter cannot be <b>NULL</b>.


### -param pRestrictToOutput [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a> interface for the swap chain to restrict content to. If the swap chain is moved to a different output, the content is black. You can optionally set this parameter to an output target that uses <a href="dxgi_present.htm">DXGI_PRESENT_RESTRICT_TO_OUTPUT</a> to restrict the content on this output. If the swap chain is moved to a different output, the content is black.

You must also pass the <a href="dxgi_present.htm">DXGI_PRESENT_RESTRICT_TO_OUTPUT</a> flag in a present call to force the content to appear blacked out on any other output. If you want to restrict the content to a different output, you must create a new swap chain. However, you can conditionally restrict content based on the <b>DXGI_PRESENT_RESTRICT_TO_OUTPUT</b> flag.

Set this parameter to <b>NULL</b> if you don't want to restrict content to an output target.


### -param ppSwapChain [out]

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a> interface for the swap chain that this method creates.


## -returns



<b>CreateSwapChainForCompositionSurfaceHandle</b> returns:
        <ul>
<li>S_OK if it successfully created a swap chain.</li>
<li>E_OUTOFMEMORY if memory is unavailable to complete the operation.</li>
<li>
<a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_INVALID_CALL</a>  if the calling application provided invalid data, for example, if <i>pDesc</i>, <i>pYuvDecodeBuffers</i>, or <i>ppSwapChain</i> is <b>NULL</b>.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic that are defined by the type of device that you pass to <i>pDevice</i>.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/B6B92F4F-B1D0-40B9-987D-F0C0F2CC7AD1">For best performance, use DXGI flip model</a>



<a href="https://msdn.microsoft.com/5646B34D-EB2C-4161-8FF0-67F96254AFBC">IDXGIFactoryMedia</a>
 

 

