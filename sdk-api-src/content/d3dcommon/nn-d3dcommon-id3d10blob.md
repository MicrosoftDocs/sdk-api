---
UID: NN:d3dcommon.ID3D10Blob
title: ID3D10Blob
author: windows-driver-content
description: This interface is used to return arbitrary length data.
old-location: direct3d10\id3d10blob.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10blob.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 45a3b1ec-c6a6-dde6-52cf-6833c6a062ee, ID3D10Blob, ID3D10Blob interface [Direct3D 10], ID3D10Blob interface [Direct3D 10], described, d3dcommon/ID3D10Blob, direct3d10.id3d10blob
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3dcommon.h
req.include-header: 
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
req.typenames: D3D_SHADER_VARIABLE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10Blob
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D10Blob interface


## -description


This interface is used to return arbitrary length data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Blob</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D10Blob</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10Blob</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1633d3ae-6002-4248-89be-74fe2657d65f">GetBufferPointer</a>
</td>
<td align="left" width="63%">
Get a pointer to the data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa47ec94-01e8-4e4b-a00a-2a0aca17c58a">GetBufferSize</a>
</td>
<td align="left" width="63%">
Get the size.

</td>
</tr>
</table> 


## -remarks



An <b>ID3D10Blob</b> is obtained by calling <a href="https://msdn.microsoft.com/bacc1d17-13e2-428c-9fd5-01c02406aa14">D3D10CreateBlob</a>.

The  <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface is type defined in the  D3DCommon.h header file as a  <b>ID3D10Blob</b> interface, which is fully defined in the  D3DCommon.h header file. <b>ID3DBlob</b> is version neutral and can be used in code for any Direct3D version.

Blobs can be used as a data buffer, storing vertex, adjacency, and material information during mesh optimization and loading operations. Also, these objects are used to return object code and error messages in APIs that compile vertex, geometry and pixel shaders.




## -see-also




<a href="https://msdn.microsoft.com/f5ad2db8-da90-4bcd-83a7-7466723a9c3c">Core Interfaces</a>
 

 

