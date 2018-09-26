---
UID: NN:d3d9.IDirect3DVertexDeclaration9
title: IDirect3DVertexDeclaration9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DVertexDeclaration9 interface to encapsulate the vertex shader declaration.
old-location: direct3d9\idirect3dvertexdeclaration9.htm
tech.root: Direct3D9
ms.assetid: VS|directx_sdk|~\idirect3dvertexdeclaration9.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IDirect3DVertexDeclaration9, IDirect3DVertexDeclaration9 interface [Direct3D 9], IDirect3DVertexDeclaration9 interface [Direct3D 9],described, d3d9helper/IDirect3DVertexDeclaration9, direct3d9.idirect3dvertexdeclaration9, f42aaa68-f7f3-0eec-ac4e-7d8617f131ae
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.lib: D3d9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.lib
 - d3d9.dll
api_name:
 - IDirect3DVertexDeclaration9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DVertexDeclaration9 interface


## -description


Applications use the methods of the IDirect3DVertexDeclaration9 interface to encapsulate the vertex shader declaration.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DVertexDeclaration9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirect3DVertexDeclaration9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DVertexDeclaration9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff80439b-38fb-47f0-ad38-429decd0d573">GetDeclaration</a>
</td>
<td align="left" width="63%">
Gets the vertex shader declaration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c183de38-ab09-4a8b-951a-b12ab4e6de26">GetDevice</a>
</td>
<td align="left" width="63%">
Gets the current device.

</td>
</tr>
</table> 


## -remarks



A vertex shader declaration is made up of an array of vertex elements.

The LPDIRECT3DVERTEXDECLARATION9 and PDIRECT3DVERTEXDECLARATION9 types are defined as pointers to the <b>IDirect3DVertexDeclaration9</b> interface.
    
            


```
typedef struct IDirect3DVertexDeclaration9 *LPDIRECT3DVERTEXDECLARATION9, *PDIRECT3DVERTEXDECLARATION9;
```





## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>
 

 

