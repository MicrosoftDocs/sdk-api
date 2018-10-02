---
UID: NF:d3d9.IDirect3DDevice9.DeletePatch
title: IDirect3DDevice9::DeletePatch
author: windows-sdk-content
description: Frees a cached high-order patch.
old-location: direct3d9\idirect3ddevice9__deletepatch.htm
tech.root: Direct3D9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__deletepatch.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 2eb17a58-7131-6669-67fe-a5a0226a6e9c, DeletePatch, DeletePatch method [Direct3D 9], DeletePatch method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DeletePatch method, IDirect3DDevice9.DeletePatch, IDirect3DDevice9::DeletePatch, d3d9helper/IDirect3DDevice9::DeletePatch, direct3d9.idirect3ddevice9__deletepatch
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# IDirect3DDevice9::DeletePatch


## -description


Frees a cached high-order patch.


## -parameters




### -param Handle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Handle of the cached high-order patch to delete. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be 
     D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174373(v=VS.85).aspx">IDirect3DDevice9::DrawRectPatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174374(v=VS.85).aspx">IDirect3DDevice9::DrawTriPatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb206314(v=VS.85).aspx">Using Higher-Order Primitives (Direct3D 9)</a>
 

 

