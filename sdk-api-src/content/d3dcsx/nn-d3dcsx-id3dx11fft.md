---
UID: NN:d3dcsx.ID3DX11FFT
title: ID3DX11FFT
author: windows-sdk-content
description: Encapsulates forward and inverse FFTs.
old-location: direct3d11\id3dx11fft.htm
tech.root: direct3d11
ms.assetid: 6979aea4-5121-4a65-85f6-4b5753083715
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 6baaded3-822f-0135-c977-9d5552c9ac99, ID3DX11FFT, ID3DX11FFT interface [Direct3D 11], ID3DX11FFT interface [Direct3D 11],described, d3dcsx/ID3DX11FFT, direct3d11.id3dx11fft
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3dcsx.h
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
req.lib: D3dcsx.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3dcsx.lib
 - d3dcsx.dll
api_name:
 - ID3DX11FFT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3DX11FFT interface


## -description


Encapsulates forward and inverse FFTs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3DX11FFT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3DX11FFT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3DX11FFT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50c714fc-91fb-4a7d-a430-40ff221a1a14">AttachBuffersAndPrecompute</a>
</td>
<td align="left" width="63%">
Attaches buffers to an FFT context and performs any required precomputations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da10b166-9561-4c04-b6b8-92b2daec30d7">ForwardTransform</a>
</td>
<td align="left" width="63%">
Performs a forward FFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d66cef71-df1e-40fa-80ba-9e0813608ee2">GetForwardScale</a>
</td>
<td align="left" width="63%">
Gets the scale for forward transforms.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ec8f0c6-7c7a-481b-b751-523ed82726c9">GetInverseScale</a>
</td>
<td align="left" width="63%">
Get the scale for inverse transforms.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4fe7a35-b039-4977-ba68-9869c5cc4383">InverseTransform</a>
</td>
<td align="left" width="63%">
Performs an inverse FFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afca03bb-459f-42ff-bc88-7487b1bc250d">SetForwardScale</a>
</td>
<td align="left" width="63%">
Sets the scale used for forward transforms.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db29b6f8-ee36-48b6-8e28-f4bbaa6b0a7f">SetInverseScale</a>
</td>
<td align="left" width="63%">
Sets the scale used for inverse transforms.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/A4F5E487-AA6C-4C64-90CF-88587F2E8B8B">D3DCSX 11 Interfaces</a>
 

 

