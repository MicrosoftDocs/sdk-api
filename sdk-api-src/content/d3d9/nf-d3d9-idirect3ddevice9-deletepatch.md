---
UID: NF:d3d9.IDirect3DDevice9.DeletePatch
title: IDirect3DDevice9::DeletePatch (d3d9.h)
author: windows-sdk-content
description: Frees a cached high-order patch.
old-location: direct3d9\idirect3ddevice9__deletepatch.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__deletepatch.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 2eb17a58-7131-6669-67fe-a5a0226a6e9c, DeletePatch, DeletePatch method [Direct3D 9], DeletePatch method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DeletePatch method, IDirect3DDevice9.DeletePatch, IDirect3DDevice9::DeletePatch, d3d9helper/IDirect3DDevice9::DeletePatch, direct3d9.idirect3ddevice9__deletepatch
ms.topic: method
f1_keywords: 
 - "d3d9/IDirect3DDevice9.DeletePatch"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.DeletePatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DDevice9::DeletePatch


## -description


Frees a cached high-order patch.


## -parameters




### -param Handle [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Handle of the cached high-order patch to delete. 


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be 
     D3DERR_INVALIDCALL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawrectpatch">IDirect3DDevice9::DrawRectPatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawtripatch">IDirect3DDevice9::DrawTriPatch</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/using-higher-order-primitives">Using Higher-Order Primitives (Direct3D 9)</a>
 

 

