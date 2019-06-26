---
UID: NN:d3d9helper.IDirect3DPixelShader9
title: IDirect3DPixelShader9 (d3d9helper.h)
author: windows-sdk-content
description: Applications use the methods of the IDirect3DPixelShader9 interface to encapsulate the functionality of a pixel shader.
old-location: direct3d9\idirect3dpixelshader9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dpixelshader9.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 1b9d322d-ffbe-622f-e100-b394c60f0d5d, IDirect3DPixelShader9, IDirect3DPixelShader9 interface [Direct3D 9], IDirect3DPixelShader9 interface [Direct3D 9],described, d3d9helper/IDirect3DPixelShader9, direct3d9.idirect3dpixelshader9
ms.topic: interface
f1_keywords: 
 - "d3d9helper/IDirect3DPixelShader9"
req.header: d3d9helper.h
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
 - IDirect3DPixelShader9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DPixelShader9 interface


## -description


Applications use the methods of the IDirect3DPixelShader9 interface to encapsulate the functionality of a pixel shader.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DPixelShader9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3DPixelShader9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DPixelShader9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dpixelshader9-getdevice">GetDevice</a>
</td>
<td align="left" width="63%">
Gets the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dpixelshader9-getfunction">GetFunction</a>
</td>
<td align="left" width="63%">
Gets a pointer to the shader data.

</td>
</tr>
</table> 


## -remarks



The LPDIRECT3DPIXELSHADER9 and PDIRECT3DPIXELSHADER9 types are defined as pointers to the <b>IDirect3DPixelShader9</b> interface.
    
            


```
typedef struct IDirect3DPixelShader9 *LPDIRECT3DPIXELSHADER9, *PDIRECT3DPIXELSHADER9;
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>
 

 

