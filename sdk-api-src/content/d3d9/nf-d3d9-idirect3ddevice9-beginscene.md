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

# IDirect3DDevice9::BeginScene


## -description


Begins a scene. 


## -parameters






## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. The method will fail with D3DERR_INVALIDCALL if <b>IDirect3DDevice9::BeginScene</b> is called 
      while already in a <b>IDirect3DDevice9::BeginScene</b>/<a href="https://msdn.microsoft.com/9ff1e40e-9e19-4168-ae29-6f7d204ab236">IDirect3DDevice9::EndScene</a> pair. This happens only 
      when <b>IDirect3DDevice9::BeginScene</b> is called twice without first calling <b>IDirect3DDevice9::EndScene</b>.




## -remarks



Applications must call <b>IDirect3DDevice9::BeginScene</b> before performing any rendering and must call <a href="https://msdn.microsoft.com/9ff1e40e-9e19-4168-ae29-6f7d204ab236">IDirect3DDevice9::EndScene</a> 
      when rendering is complete and before calling <b>IDirect3DDevice9::BeginScene</b> again.

If <b>IDirect3DDevice9::BeginScene</b> fails, the device was unable to begin the scene, and there is no need to 
      call <a href="https://msdn.microsoft.com/9ff1e40e-9e19-4168-ae29-6f7d204ab236">IDirect3DDevice9::EndScene</a>. In fact, calls to <b>IDirect3DDevice9::EndScene</b> will fail if the 
      previous <b>IDirect3DDevice9::BeginScene</b> failed. This applies to any application that creates multiple swap chains.

There should be one <b>IDirect3DDevice9::BeginScene</b>/<a href="https://msdn.microsoft.com/9ff1e40e-9e19-4168-ae29-6f7d204ab236">IDirect3DDevice9::EndScene</a> pair between any successive calls to 
      present (either <a href="https://msdn.microsoft.com/47e67956-7ab4-4e05-bf05-685bdc094cf2">IDirect3DDevice9::Present</a> or <a href="https://msdn.microsoft.com/ac90aee6-dd66-46d8-a628-4bf8bff087b4">IDirect3DSwapChain9::Present</a>). <b>IDirect3DDevice9::BeginScene</b> should 
      be called once before any rendering is performed, and <b>IDirect3DDevice9::EndScene</b> should be called once after all rendering for a frame has been
      submitted to the runtime. Multiple non-nested <b>IDirect3DDevice9::BeginScene</b>/<b>IDirect3DDevice9::EndScene</b> pairs between calls to present
      are legal, but having more than one pair may incur a performance hit.
      To enable maximal parallelism between the CPU and the graphics accelerator, it is advantageous to 
      call <b>IDirect3DDevice9::EndScene</b> as far ahead of calling present as possible.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

