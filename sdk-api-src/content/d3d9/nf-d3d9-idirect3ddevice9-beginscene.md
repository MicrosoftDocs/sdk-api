---
UID: NF:d3d9.IDirect3DDevice9.BeginScene
title: IDirect3DDevice9::BeginScene (d3d9.h)
description: The IDirect3DDevice9::BeginScene method (d3d9.h) begins a scene.
helpviewer_keywords: ["0d9bef66-554d-4515-e088-ddeeef8f07b9","BeginScene","BeginScene method [Direct3D 9]","BeginScene method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","BeginScene method","IDirect3DDevice9.BeginScene","IDirect3DDevice9::BeginScene","d3d9helper/IDirect3DDevice9::BeginScene","direct3d9.idirect3ddevice9__beginscene"]
old-location: direct3d9\idirect3ddevice9__beginscene.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__beginscene.htm
ms.date: 08/10/2022
ms.keywords: 0d9bef66-554d-4515-e088-ddeeef8f07b9, BeginScene, BeginScene method [Direct3D 9], BeginScene method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],BeginScene method, IDirect3DDevice9.BeginScene, IDirect3DDevice9::BeginScene, d3d9helper/IDirect3DDevice9::BeginScene, direct3d9.idirect3ddevice9__beginscene
req.header: d3d9.h
req.include-header: D3D9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9::BeginScene
 - d3d9/IDirect3DDevice9::BeginScene
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.BeginScene
---

# IDirect3DDevice9::BeginScene


## -description

Begins a scene.



## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. The method will fail with D3DERR_INVALIDCALL if <b>IDirect3DDevice9::BeginScene</b> is called 
      while already in a <b>IDirect3DDevice9::BeginScene</b>/<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene">IDirect3DDevice9::EndScene</a> pair. This happens only 
      when <b>IDirect3DDevice9::BeginScene</b> is called twice without first calling <b>IDirect3DDevice9::EndScene</b>.

## -remarks

Applications must call <b>IDirect3DDevice9::BeginScene</b> before performing any rendering and must call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene">IDirect3DDevice9::EndScene</a> 
      when rendering is complete and before calling <b>IDirect3DDevice9::BeginScene</b> again.

If <b>IDirect3DDevice9::BeginScene</b> fails, the device was unable to begin the scene, and there is no need to 
      call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene">IDirect3DDevice9::EndScene</a>. In fact, calls to <b>IDirect3DDevice9::EndScene</b> will fail if the 
      previous <b>IDirect3DDevice9::BeginScene</b> failed. This applies to any application that creates multiple swap chains.

There should be one <b>IDirect3DDevice9::BeginScene</b>/<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene">IDirect3DDevice9::EndScene</a> pair between any successive calls to 
      present (either <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-present">IDirect3DDevice9::Present</a> or <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present">IDirect3DSwapChain9::Present</a>). <b>IDirect3DDevice9::BeginScene</b> should 
      be called once before any rendering is performed, and <b>IDirect3DDevice9::EndScene</b> should be called once after all rendering for a frame has been
      submitted to the runtime. Multiple non-nested <b>IDirect3DDevice9::BeginScene</b>/<b>IDirect3DDevice9::EndScene</b> pairs between calls to present
      are legal, but having more than one pair may incur a performance hit.
      To enable maximal parallelism between the CPU and the graphics accelerator, it is advantageous to 
      call <b>IDirect3DDevice9::EndScene</b> as far ahead of calling present as possible.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
