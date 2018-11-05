---
UID: NF:d3d9.IDirect3DVertexDeclaration9.GetDeclaration
title: IDirect3DVertexDeclaration9::GetDeclaration
author: windows-sdk-content
description: Gets the vertex shader declaration.
old-location: direct3d9\idirect3dvertexdeclaration9__getdeclaration.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvertexdeclaration9__getdeclaration.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetDeclaration, GetDeclaration method [Direct3D 9], GetDeclaration method [Direct3D 9],IDirect3DVertexDeclaration9 interface, IDirect3DVertexDeclaration9 interface [Direct3D 9],GetDeclaration method, IDirect3DVertexDeclaration9.GetDeclaration, IDirect3DVertexDeclaration9::GetDeclaration, bd1cb4cd-85cf-525d-1ac3-ebd3eb527b1a, d3d9helper/IDirect3DVertexDeclaration9::GetDeclaration, direct3d9.idirect3dvertexdeclaration9__getdeclaration
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
 - IDirect3DVertexDeclaration9.GetDeclaration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DVertexDeclaration9::GetDeclaration


## -description


Gets the vertex shader declaration.


## -parameters




### -param pElement

TBD


### -param pNumElements [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Number of elements in the array. The application needs to allocate enough room for this. 


#### - arg1 [in, out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172630(v=VS.85).aspx">D3DVERTEXELEMENT9</a>*</b>

Array of vertex elements (see <a href="https://msdn.microsoft.com/en-us/library/Bb172630(v=VS.85).aspx">D3DVERTEXELEMENT9</a>) that make up a vertex shader declaration. The application needs to allocate enough room for this. The vertex element array ends with the <a href="https://msdn.microsoft.com/en-us/library/Bb172535(v=VS.85).aspx">D3DDECL_END</a> macro.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be:
     D3DERR_INVALIDCALL.




## -remarks



The number of elements, pNumElements, includes the <a href="https://msdn.microsoft.com/en-us/library/Bb172535(v=VS.85).aspx">D3DDECL_END</a> macro, which ends the declaration. So the element count is actually one higher than the number of valid vertex elements.

Here's an example that will return the vertex declaration array of up to 256 elements:


```
 
D3DVERTEXELEMENT9 decl[MAXD3DDECLLENGTH];
UINT numElements;
HRESULT hr = m_pVertexDeclaration->GetDeclaration( decl, &numElements);

```


Specify <b>NULL</b> for pDeclto get the number of elements in the declaration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205919(v=VS.85).aspx">IDirect3DVertexDeclaration9</a>
 

 

