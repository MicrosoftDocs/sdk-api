---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D11DeviceContext::Flush


## -description


Sends queued-up commands in the command buffer to the graphics processing unit (GPU).


## -parameters






## -returns



This method does not return a value.




## -remarks



Most applications don't need to call this method. If an application calls this method when not necessary, it incurs a performance penalty. 
      Each call to <b>Flush</b> incurs a significant amount of overhead.

When Microsoft Direct3D state-setting, present, or draw commands are called by an application, those commands are queued into an internal command buffer. 
      <b>Flush</b> sends those commands to the GPU for processing. Typically, the Direct3D runtime sends these commands to the GPU automatically whenever the runtime determines that 
      they need to be sent, such as when the command buffer is full or when an application maps a resource. <b>Flush</b> sends the commands manually.

We recommend that you use <b>Flush</b> when the CPU waits for an arbitrary amount of time (such as when 
      you call the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439324">Sleep</a> function).

Because <b>Flush</b> operates asynchronously,  it can return either before or after the GPU finishes executing the queued graphics commands. However, the graphics commands eventually always complete. You can call the <a href="https://msdn.microsoft.com/ad09a309-862f-462d-8268-62e44397c298">ID3D11Device::CreateQuery</a> method with the <a href="d3d11_query.htm">D3D11_QUERY_EVENT</a> value to create an event query; you can then use that event query in a call to the <a href="https://msdn.microsoft.com/338d02ad-2227-49e5-9b4f-fb86a3898f73">ID3D11DeviceContext::GetData</a> method to determine when the GPU is finished processing the graphics commands.


Microsoft Direct3D 11 defers the destruction of objects. Therefore, an application can't rely upon objects immediately being destroyed. By calling <b>Flush</b>, you destroy any 
      objects whose destruction was deferred.  If an application requires synchronous destruction of an object, we recommend that the application release all its
      references, call <a href="https://msdn.microsoft.com/dabf52f5-0f69-4017-863c-9e3ecef4d5dc">ID3D11DeviceContext::ClearState</a>, and then call <b>Flush</b>.

<h3><a id="Defer_Issues_with_Flip"></a><a id="defer_issues_with_flip"></a><a id="DEFER_ISSUES_WITH_FLIP"></a>Deferred Destruction Issues with Flip Presentation Swap Chains</h3>
Direct3D 11 defers the destruction of objects like views and resources until it can efficiently destroy them. This deferred destruction can cause problems with flip presentation model swap chains. Flip presentation model swap chains have the <a href="https://msdn.microsoft.com/211d53a9-1332-4e94-abd5-7df7f19094a6">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> flag set. When you create a flip presentation model swap chain, you can associate only one swap chain at a time with an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a>, <b>IWindow</b>, or composition surface. If an application attempts to destroy a flip presentation model swap chain and replace it with another swap chain, the original swap chain is not destroyed when the application immediately frees all of the original swap chain's references.

Most applications typically use the <a href="https://msdn.microsoft.com/c70aaad0-e742-4ff1-9d25-80d171f3f9de">IDXGISwapChain::ResizeBuffers</a> method for the majority of scenarios where they replace new swap chain buffers for old swap chain buffers. However, if an application must actually destroy an old swap chain and create a new swap chain, the application must force the destruction of all objects that the application freed. To force the destruction, call <a href="https://msdn.microsoft.com/dabf52f5-0f69-4017-863c-9e3ecef4d5dc">ID3D11DeviceContext::ClearState</a> (or otherwise ensure no views are bound to pipeline state), and then call <b>Flush</b> on the immediate context. You must force destruction before you call <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, or <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a> again to create a new swap chain.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

