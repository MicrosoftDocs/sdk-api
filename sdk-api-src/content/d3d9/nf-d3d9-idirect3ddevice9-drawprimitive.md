---
UID: NF:d3d9.IDirect3DDevice9.DrawPrimitive
title: IDirect3DDevice9::DrawPrimitive
author: windows-sdk-content
description: Renders a sequence of nonindexed, geometric primitives of the specified type from the current set of data input streams.
old-location: direct3d9\idirect3ddevice9__drawprimitive.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__drawprimitive.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: DrawPrimitive, DrawPrimitive method [Direct3D 9], DrawPrimitive method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DrawPrimitive method, IDirect3DDevice9.DrawPrimitive, IDirect3DDevice9::DrawPrimitive, d3d9helper/IDirect3DDevice9::DrawPrimitive, direct3d9.idirect3ddevice9__drawprimitive, f6573fdd-1724-cbca-56a1-0b336470257e
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.DrawPrimitive
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::DrawPrimitive


## -description


Renders a sequence of nonindexed, geometric primitives of the specified type from the current set of data input streams.


## -parameters




### -param PrimitiveType [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172589(v=VS.85).aspx">D3DPRIMITIVETYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172589(v=VS.85).aspx">D3DPRIMITIVETYPE</a> enumerated type, describing the type of primitive to render. 


### -param StartVertex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the first vertex to load. Beginning at StartVertex the correct number of vertices will be read out of the vertex buffer. 


### -param PrimitiveCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of primitives to render. The maximum number of primitives allowed is determined by checking the MaxPrimitiveCount member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172513(v=VS.85).aspx">D3DCAPS9</a> structure. PrimitiveCount is the number of primitives as determined by the primitive type. If it is a line list, each primitive has two vertices. If it is a triangle list, each primitive has three vertices. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be 
     D3DERR_INVALIDCALL.




## -remarks



When converting a legacy application to Direct3D 9, you must add a call to either <a href="https://msdn.microsoft.com/en-us/library/Bb174433(v=VS.85).aspx">IDirect3DDevice9::SetFVF</a> to use the fixed function pipeline, or <a href="https://msdn.microsoft.com/en-us/library/Bb174464(v=VS.85).aspx">IDirect3DDevice9::SetVertexDeclaration</a> to use a vertex shader before you make any Draw calls.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174369(v=VS.85).aspx">IDirect3DDevice9::DrawIndexedPrimitive</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb147325(v=VS.85).aspx">Rendering from Vertex and Index Buffers (Direct3D 9)</a>
 

 

