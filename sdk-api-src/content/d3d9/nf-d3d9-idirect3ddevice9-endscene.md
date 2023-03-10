---
UID: NF:d3d9.IDirect3DDevice9.EndScene
title: IDirect3DDevice9::EndScene (d3d9.h)
description: The IDirect3DDevice9::EndScene method (d3d9.h) ends a scene that was begun by calling IDirect3DDevice9::BeginScene.
helpviewer_keywords: ["5a0213d4-1bba-e7fc-0a90-704668833b85","EndScene","EndScene method [Direct3D 9]","EndScene method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","EndScene method","IDirect3DDevice9.EndScene","IDirect3DDevice9::EndScene","d3d9helper/IDirect3DDevice9::EndScene","direct3d9.idirect3ddevice9__endscene"]
old-location: direct3d9\idirect3ddevice9__endscene.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__endscene.htm
ms.date: 08/10/2022
ms.keywords: 5a0213d4-1bba-e7fc-0a90-704668833b85, EndScene, EndScene method [Direct3D 9], EndScene method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],EndScene method, IDirect3DDevice9.EndScene, IDirect3DDevice9::EndScene, d3d9helper/IDirect3DDevice9::EndScene, direct3d9.idirect3ddevice9__endscene
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
 - IDirect3DDevice9::EndScene
 - d3d9/IDirect3DDevice9::EndScene
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
 - IDirect3DDevice9.EndScene
---

# IDirect3DDevice9::EndScene


## -description

Ends a scene that was begun by calling <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-beginscene">IDirect3DDevice9::BeginScene</a>.



## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. The method will fail with D3DERR_INVALIDCALL if <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-beginscene">IDirect3DDevice9::BeginScene</a> is called while already in a <b>IDirect3DDevice9::BeginScene</b>/<b>IDirect3DDevice9::EndScene</b> pair. This happens only when <b>IDirect3DDevice9::BeginScene</b> is called twice without first calling <b>IDirect3DDevice9::EndScene</b>.

## -remarks

When this method succeeds, the scene has been queued up for rendering by the driver. This is not a synchronous method, so the scene is not guaranteed to have completed rendering when this method returns.

Applications must call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-beginscene">IDirect3DDevice9::BeginScene</a> before performing any rendering and must call <b>IDirect3DDevice9::EndScene</b> when rendering is complete and before calling <b>IDirect3DDevice9::BeginScene</b> again.

If <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-beginscene">IDirect3DDevice9::BeginScene</a> fails, the device was unable to begin the scene, and there is no need to call <b>IDirect3DDevice9::EndScene</b>. In fact, calls to 
    
<b>IDirect3DDevice9::EndScene</b> will fail if the previous <b>IDirect3DDevice9::BeginScene</b> failed. This applies to any application that creates multiple swap chains.

There should be at most one <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-beginscene">IDirect3DDevice9::BeginScene</a>/<b>IDirect3DDevice9::EndScene</b> pair between any successive calls to present (either <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-present">IDirect3DDevice9::Present</a> or <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present">IDirect3DSwapChain9::Present</a>). <b>IDirect3DDevice9::BeginScene</b> should be called once before any rendering is performed, and <b>IDirect3DDevice9::EndScene</b> should be called once after all rendering for a frame has been submitted to the runtime. To enable maximal parallelism between the CPU and the graphics accelerator, it is advantageous to call <b>IDirect3DDevice9::EndScene</b> as far ahead of calling present as possible.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
