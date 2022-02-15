---
UID: NF:d3d11.ID3D11DeviceContext.Flush
title: ID3D11DeviceContext::Flush (d3d11.h)
description: Sends queued-up commands in the command buffer to the graphics processing unit (GPU).
helpviewer_keywords: ["Flush","Flush method [Direct3D 11]","Flush method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","Flush method","ID3D11DeviceContext.Flush","ID3D11DeviceContext::Flush","b14698ec-f6ed-febc-05d4-5a02d568e816","d3d11/ID3D11DeviceContext::Flush","direct3d11.id3d11devicecontext_flush"]
old-location: direct3d11\id3d11devicecontext_flush.htm
tech.root: direct3d11
ms.assetid: e204c585-4996-4274-a654-b9912e957fe6
ms.date: 12/05/2018
ms.keywords: Flush, Flush method [Direct3D 11], Flush method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],Flush method, ID3D11DeviceContext.Flush, ID3D11DeviceContext::Flush, b14698ec-f6ed-febc-05d4-5a02d568e816, d3d11/ID3D11DeviceContext::Flush, direct3d11.id3d11devicecontext_flush
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::Flush
 - d3d11/ID3D11DeviceContext::Flush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.Flush
---

# ID3D11DeviceContext::Flush


## -description

Sends queued-up commands in the command buffer to the graphics processing unit (GPU).



## -remarks

Most applications don't need to call this method. If an application calls this method when not necessary, it incurs a performance penalty. 
      Each call to <b>Flush</b> incurs a significant amount of overhead.

When Microsoft Direct3D state-setting, present, or draw commands are called by an application, those commands are queued into an internal command buffer. 
      <b>Flush</b> sends those commands to the GPU for processing. Typically, the Direct3D runtime sends these commands to the GPU automatically whenever the runtime determines that 
      they need to be sent, such as when the command buffer is full or when an application maps a resource. <b>Flush</b> sends the commands manually.

We recommend that you use <b>Flush</b> when the CPU waits for an arbitrary amount of time (such as when 
      you call the <a href="/windows/desktop/api/synchapi/nf-synchapi-sleep">Sleep</a> function).

Because <b>Flush</b> operates asynchronously,  it can return either before or after the GPU finishes executing the queued graphics commands. However, the graphics commands eventually always complete. You can call the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createquery">ID3D11Device::CreateQuery</a> method with the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_query">D3D11_QUERY_EVENT</a> value to create an event query; you can then use that event query in a call to the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> method to determine when the GPU is finished processing the graphics commands.


Microsoft Direct3D 11 defers the destruction of objects. Therefore, an application can't rely upon objects immediately being destroyed. By calling <b>Flush</b>, you destroy any 
      objects whose destruction was deferred.  If an application requires synchronous destruction of an object, we recommend that the application release all its
      references, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate">ID3D11DeviceContext::ClearState</a>, and then call <b>Flush</b>.

<h3><a id="Defer_Issues_with_Flip"></a><a id="defer_issues_with_flip"></a><a id="DEFER_ISSUES_WITH_FLIP"></a>Deferred Destruction Issues with Flip Presentation Swap Chains</h3>
Direct3D 11 defers the destruction of objects like views and resources until it can efficiently destroy them. This deferred destruction can cause problems with flip presentation model swap chains. Flip presentation model swap chains have the <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> flag set. When you create a flip presentation model swap chain, you can associate only one swap chain at a time with an <a href="/windows/desktop/WinProg/windows-data-types">HWND</a>, <b>IWindow</b>, or composition surface. If an application attempts to destroy a flip presentation model swap chain and replace it with another swap chain, the original swap chain is not destroyed when the application immediately frees all of the original swap chain's references.

Most applications typically use the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers">IDXGISwapChain::ResizeBuffers</a> method for the majority of scenarios where they replace new swap chain buffers for old swap chain buffers. However, if an application must actually destroy an old swap chain and create a new swap chain, the application must force the destruction of all objects that the application freed. To force the destruction, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate">ID3D11DeviceContext::ClearState</a> (or otherwise ensure no views are bound to pipeline state), and then call <b>Flush</b> on the immediate context. You must force destruction before you call <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, or <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a> again to create a new swap chain.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
