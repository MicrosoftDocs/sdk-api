---
UID: NF:d3d9.IDirect3DDevice9.GetVertexDeclaration
title: IDirect3DDevice9::GetVertexDeclaration
author: windows-sdk-content
description: Gets a vertex shader declaration.
old-location: direct3d9\idirect3ddevice9__getvertexdeclaration.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getvertexdeclaration.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 8b909692-06a8-7089-4aa2-4693ff481d81, GetVertexDeclaration, GetVertexDeclaration method [Direct3D 9], GetVertexDeclaration method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetVertexDeclaration method, IDirect3DDevice9.GetVertexDeclaration, IDirect3DDevice9::GetVertexDeclaration, d3d9helper/IDirect3DDevice9::GetVertexDeclaration, direct3d9.idirect3ddevice9__getvertexdeclaration
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
 - IDirect3DDevice9.GetVertexDeclaration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::GetVertexDeclaration


## -description


Gets a vertex shader declaration.


## -parameters




### -param ppDecl [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205919(v=VS.85).aspx">IDirect3DVertexDeclaration9</a>**</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb205919(v=VS.85).aspx">IDirect3DVertexDeclaration9</a> object that is returned.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.
 The return value can be D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174464(v=VS.85).aspx">IDirect3DDevice9::SetVertexDeclaration</a>
 

 

