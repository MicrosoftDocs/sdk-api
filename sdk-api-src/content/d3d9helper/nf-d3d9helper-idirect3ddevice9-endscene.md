---
UID: NF:d3d9helper.IDirect3DDevice9.EndScene
title: IDirect3DDevice9::EndScene
author: windows-sdk-content
description: Ends a scene that was begun by calling IDirect3DDevice9::BeginScene.
old-location: direct3d9\idirect3ddevice9__endscene.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__endscene.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 5a0213d4-1bba-e7fc-0a90-704668833b85, EndScene, EndScene method [Direct3D 9], EndScene method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],EndScene method, IDirect3DDevice9.EndScene, IDirect3DDevice9::EndScene, d3d9helper/IDirect3DDevice9::EndScene, direct3d9.idirect3ddevice9__endscene
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
req.redist: 
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
tech.root: 
req.typenames: D3DVSHADERCAPS2_0
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
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::EndScene


## -description


Ends a scene that was begun by calling <a href="https://msdn.microsoft.com/en-us/library/Bb174350(v=VS.85).aspx">IDirect3DDevice9::BeginScene</a>.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. The method will fail with D3DERR_INVALIDCALL if <a href="https://msdn.microsoft.com/en-us/library/Bb174350(v=VS.85).aspx">IDirect3DDevice9::BeginScene</a> is called while already in a <b>IDirect3DDevice9::BeginScene</b>/<b>IDirect3DDevice9::EndScene</b> pair. This happens only when <b>IDirect3DDevice9::BeginScene</b> is called twice without first calling <b>IDirect3DDevice9::EndScene</b>.




## -remarks



When this method succeeds, the scene has been queued up for rendering by the driver. This is not a synchronous method, so the scene is not guaranteed to have completed rendering when this method returns.

Applications must call <a href="https://msdn.microsoft.com/en-us/library/Bb174350(v=VS.85).aspx">IDirect3DDevice9::BeginScene</a> before performing any rendering and must call <b>IDirect3DDevice9::EndScene</b> when rendering is complete and before calling <b>IDirect3DDevice9::BeginScene</b> again.

If <a href="https://msdn.microsoft.com/en-us/library/Bb174350(v=VS.85).aspx">IDirect3DDevice9::BeginScene</a> fails, the device was unable to begin the scene, and there is no need to call <b>IDirect3DDevice9::EndScene</b>. In fact, calls to 
    
    <b>IDirect3DDevice9::EndScene</b> will fail if the previous <b>IDirect3DDevice9::BeginScene</b> failed. This applies to any application that creates multiple swap chains.

There should be at most one <a href="https://msdn.microsoft.com/en-us/library/Bb174350(v=VS.85).aspx">IDirect3DDevice9::BeginScene</a>/<b>IDirect3DDevice9::EndScene</b> pair between any successive calls to present (either <a href="https://msdn.microsoft.com/en-us/library/Bb174423(v=VS.85).aspx">IDirect3DDevice9::Present</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb205908(v=VS.85).aspx">IDirect3DSwapChain9::Present</a>). <b>IDirect3DDevice9::BeginScene</b> should be called once before any rendering is performed, and <b>IDirect3DDevice9::EndScene</b> should be called once after all rendering for a frame has been submitted to the runtime. To enable maximal parallelism between the CPU and the graphics accelerator, it is advantageous to call <b>IDirect3DDevice9::EndScene</b> as far ahead of calling present as possible.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>
 

 

