---
UID: NF:dxgi1_3.IDXGIFactoryMedia.CreateDecodeSwapChainForCompositionSurfaceHandle
title: IDXGIFactoryMedia::CreateDecodeSwapChainForCompositionSurfaceHandle
author: windows-sdk-content
description: Creates a YUV swap chain for an existing DirectComposition surface handle.
old-location: direct3ddxgi\idxgifactorymedia_createdecodeswapchainforcompositionsurfacehandle.htm
tech.root: direct3ddxgi
ms.assetid: A4030D6E-EE5A-47E7-A5A2-A008F6869230
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CreateDecodeSwapChainForCompositionSurfaceHandle, CreateDecodeSwapChainForCompositionSurfaceHandle method [DXGI], CreateDecodeSwapChainForCompositionSurfaceHandle method [DXGI],IDXGIFactoryMedia interface, IDXGIFactoryMedia interface [DXGI],CreateDecodeSwapChainForCompositionSurfaceHandle method, IDXGIFactoryMedia.CreateDecodeSwapChainForCompositionSurfaceHandle, IDXGIFactoryMedia::CreateDecodeSwapChainForCompositionSurfaceHandle, direct3ddxgi.idxgifactorymedia_createdecodeswapchainforcompositionsurfacehandle, dxgi1_3/IDXGIFactoryMedia::CreateDecodeSwapChainForCompositionSurfaceHandle
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
 - IDXGIFactoryMedia.CreateDecodeSwapChainForCompositionSurfaceHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIFactoryMedia::CreateDecodeSwapChainForCompositionSurfaceHandle


## -description


Creates a YUV swap chain for an existing <a href="https://msdn.microsoft.com/A220189D-8546-4352-8F6F-AC5D2192940D">DirectComposition</a> surface handle.
         The swap chain is created with pre-existing buffers and very few descriptive elements are required. Instead, this method requires 
        a <a href="https://msdn.microsoft.com/A220189D-8546-4352-8F6F-AC5D2192940D">DirectComposition</a> surface handle and an <a href="https://msdn.microsoft.com/de1f11a5-194b-438e-975b-3945179d0ed7">IDXGIResource</a> 
        buffer to hold decoded frame data. The swap chain format is determined by the format of the subresources of the <b>IDXGIResource</b>.
      


## -parameters




### -param pDevice [in]

A pointer to the Direct3D device for the swap chain. This parameter cannot be <b>NULL</b>. 
            Software drivers, like <a href="https://msdn.microsoft.com/ceeec7d6-4bdc-488c-80a8-6c5e11986d6a">D3D_DRIVER_TYPE_REFERENCE</a>, are not supported for composition swap chains.
          


### -param hSurface [in, optional]

A handle to an existing <a href="https://msdn.microsoft.com/A220189D-8546-4352-8F6F-AC5D2192940D">DirectComposition</a> surface. This parameter cannot be <b>NULL</b>.
          


### -param pDesc [in]

A pointer to a  <a href="https://msdn.microsoft.com/9AAF8E99-E5BC-49B3-8CA6-1F4FC0190B54">DXGI_DECODE_SWAP_CHAIN_DESC</a> structure for the swap-chain description. 
            This parameter cannot be <b>NULL</b>.
          


### -param pYuvDecodeBuffers [in]

A pointer to a <a href="https://msdn.microsoft.com/de1f11a5-194b-438e-975b-3945179d0ed7">IDXGIResource</a> interface that represents the resource that contains the info 
            that <b>CreateDecodeSwapChainForCompositionSurfaceHandle</b> decodes.
          


### -param pRestrictToOutput [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a> interface for the swap chain to restrict content to. If the swap chain 
              is moved to a different output, the content is black. You can optionally set this parameter to an output target that 
              uses <a href="dxgi_present.htm">DXGI_PRESENT_RESTRICT_TO_OUTPUT</a> to restrict 
              the content on this output. If the swap chain is moved to a different output, the content is black.
            

You must also pass the <a href="dxgi_present.htm">DXGI_PRESENT_RESTRICT_TO_OUTPUT</a> flag in a 
              present call to force the content to appear blacked out on any other output. If you want to restrict the content to a different output, you must create a new swap chain. 
              However, you can conditionally restrict content 
              based on the <b>DXGI_PRESENT_RESTRICT_TO_OUTPUT</b> flag.
            

Set this parameter to <b>NULL</b> if you don't want to restrict content to an output target.
            


### -param ppSwapChain [out]

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/814EDDA6-EFEA-4281-BE06-9FF8822B4927">IDXGIDecodeSwapChain</a> interface for the 
            swap chain that this method creates.
          


## -returns



<b>CreateDecodeSwapChainForCompositionSurfaceHandle</b> returns:
              <ul>
<li>S_OK if it successfully created a swap chain.</li>
<li>E_OUTOFMEMORY if memory is unavailable to complete the operation.</li>
<li>
<a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_INVALID_CALL</a>  if the calling application provided invalid data, for example, 
                  if <i>pDesc</i>, <i>pYuvDecodeBuffers</i>, or <i>ppSwapChain</i> is <b>NULL</b>.
                </li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic that are defined by the type of
                  device that you pass to <i>pDevice</i>.
                </li>
</ul>





## -remarks



The <a href="https://msdn.microsoft.com/de1f11a5-194b-438e-975b-3945179d0ed7">IDXGIResource</a> provided via the <i>pYuvDecodeBuffers</i> 
      parameter must point to at least one subresource, and all subresources must be created with the <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_DECODER</a> flag.




## -see-also




<a href="https://msdn.microsoft.com/5646B34D-EB2C-4161-8FF0-67F96254AFBC">IDXGIFactoryMedia</a>
 

 

