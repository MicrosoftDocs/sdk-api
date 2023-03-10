---
UID: NF:d3d9.IDirect3DDevice9.SetFVF
title: IDirect3DDevice9::SetFVF (d3d9.h)
description: The IDirect3DDevice9::SetFVF method (d3d9.h) sets the current vertex stream declaration.
helpviewer_keywords: ["19b67e41-5ea9-7478-a24f-8698b2b106a5","IDirect3DDevice9 interface [Direct3D 9]","SetFVF method","IDirect3DDevice9.SetFVF","IDirect3DDevice9::SetFVF","SetFVF","SetFVF method [Direct3D 9]","SetFVF method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetFVF","direct3d9.idirect3ddevice9__setfvf"]
old-location: direct3d9\idirect3ddevice9__setfvf.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setfvf.htm
ms.date: 08/11/2022
ms.keywords: 19b67e41-5ea9-7478-a24f-8698b2b106a5, IDirect3DDevice9 interface [Direct3D 9],SetFVF method, IDirect3DDevice9.SetFVF, IDirect3DDevice9::SetFVF, SetFVF, SetFVF method [Direct3D 9], SetFVF method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetFVF, direct3d9.idirect3ddevice9__setfvf
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
 - IDirect3DDevice9::SetFVF
 - d3d9/IDirect3DDevice9::SetFVF
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
 - IDirect3DDevice9.SetFVF
---

# IDirect3DDevice9::SetFVF


## -description

Sets the current vertex stream declaration.

## -parameters

### -param FVF [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

DWORD containing the fixed function vertex type. For more information, see <a href="/windows/desktop/direct3d9/d3dfvf">D3DFVF</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be:
     D3DERR_INVALIDCALL.

## -remarks

Here are the steps necessary to initialize and use vertices that have a position, diffuse and specular color, and texture coordinates:

<ol>
<li>
Define the custom vertex type and FVF code.


```

struct LVertex
{
    FLOAT    x, y, z;
    D3DCOLOR specular, diffuse;
    FLOAT    tu, tv;
};
    
const DWORD VertexFVF = (D3DFVF_XYZ | D3DFVF_DIFFUSE |
                         D3DFVF_SPECULAR | D3DFVF_TEX1 );

```


</li>
<li>
Create a vertex buffer with enough room for four vertices using <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexbuffer">IDirect3DDevice9::CreateVertexBuffer</a>.
    



```

g_d3dDevice->CreateVertexBuffer( 4*sizeof(LVertex),  
    D3DUSAGE_WRITEONLY, VertexFVF, D3DPOOL_DEFAULT, &pBigSquareVB, NULL );

```


</li>
<li>
Set the values for each vertex.
    
    
    



```

LVertex * v;
pBigSquareVB->Lock( 0, 0, (BYTE**)&v, 0 );
    
v[0].x  = 0.0f;  v[0].y  = 10.0;  v[0].z  = 10.0f;
v[0].diffuse  = 0xffff0000;
v[0].specular = 0xff00ff00;
v[0].tu = 0.0f;  v[0].tv = 0.0f;
    
v[1].x  = 0.0f;  v[1].y  = 0.0f;  v[1].z  = 10.0f;
v[1].diffuse  = 0xff00ff00;
v[1].specular = 0xff00ffff;
v[1].tu = 0.0f;  v[1].tv = 0.0f;
    
v[2].x  = 10.0f; v[2].y  = 10.0f; v[2].z  = 10.0f;
v[2].diffuse  = 0xffff00ff;
v[2].specular = 0xff000000;
v[2].tu = 0.0f;  v[2].tv = 0.0f;
    
v[3].x  = 0.0f; v[3].y  = 10.0f;  v[3].z = 10.0f;
v[3].diffuse  = 0xffffff00;
v[3].specular = 0xffff0000;
v[3].tu = 0.0f; v[3].tv = 0.0f;
    
pBigSquareVB->Unlock();

```


</li>
<li>
The vertex buffer has been initialized and is ready to render. The following code example shows how to use the legacy FVF to draw a square.
    
    
    



```

g_d3dDevice->SetFVF(VertexFVF);
g_d3dDevice->SetStreamSource(0, pBigSquareVB, 0, sizeof(LVertex));
g_d3dDevice->DrawPrimitive(D3DPT_TRIANGLESTRIP, 0 ,2);

```


</li>
</ol>
Here are the steps necessary to initialize and use vertices that have a position, a normal, and texture coordinates:

<ol>
<li>
Define the custom vertex type and FVF code.


```

struct Vertex
{
    FLOAT x, y, z;
    FLOAT nx, ny, nz;
    FLOAT tu, tv;
};
    
const DWORD VertexFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_TEX1 );

```


</li>
<li>
Create a vertex buffer with enough room for four vertices using <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexbuffer">IDirect3DDevice9::CreateVertexBuffer</a> (similar to the example above).

</li>
<li>
Set the values for each vertex.
    
    
    



```

Vertex * v;
pBigSquareVB->Lock(0, 0, (BYTE**)&v, 0);
    
v[0].x  = 0.0f;  v[0].y  = 10.0;  v[0].z  = 10.0f;
v[0].nx = 0.0f;  v[0].ny = 1.0f;  v[0].nz = 0.0f;
v[0].tu = 0.0f;  v[0].tv = 0.0f;

v[1].x  = 0.0f;  v[1].y  = 0.0f;  v[1].z  = 10.0f;
v[1].nx = 0.0f;  v[1].ny = 1.0f;  v[1].nz = 0.0f;
v[1].tu = 0.0f;  v[1].tv = 0.0f;
    
v[2].x  = 10.0f; v[2].y  = 10.0f; v[2].z  = 10.0f;
v[2].nx = 0.0f;  v[2].ny = 1.0f;  v[2].nz = 0.0f;
v[2].tu = 0.0f;  v[2].tv = 0.0f;
    
v[3].x  = 0.0f; v[3].y  = 10.0f;  v[3].z = 10.0f;
v[3].nx = 0.0f; v[3].ny = 1.0f;   v[3].nz = 0.0f;
v[3].tu = 0.0f; v[3].tv = 0.0f;
    
pBigSquareVB->Unlock();

```


</li>
<li>Draw the object (similar to the example above).</li>
</ol>

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getfvf">IDirect3DDevice9::GetFVF</a>
