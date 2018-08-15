---
UID: NN:d3d10effect.ID3D10EffectConstantBuffer
title: ID3D10EffectConstantBuffer
author: windows-sdk-content
description: A constant-buffer interface accesses constant buffers or texture buffers.
old-location: direct3d10\id3d10effectconstantbuffer.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectconstantbuffer.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 03babb38-8c88-954d-43c3-eb8942a15d5a, ID3D10EffectConstantBuffer, ID3D10EffectConstantBuffer interface [Direct3D 10], ID3D10EffectConstantBuffer interface [Direct3D 10],described, d3d10effect/ID3D10EffectConstantBuffer, direct3d10.id3d10effectconstantbuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d10effect.h
req.include-header: 
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10EffectConstantBuffer
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10EffectConstantBuffer interface


## -description


A constant-buffer interface accesses constant buffers or texture buffers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10EffectConstantBuffer</b> interface inherits from <a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable</a>. <b>ID3D10EffectConstantBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10EffectConstantBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b1bf2a6-3be8-4c5a-81a0-52195af180ee">GetConstantBuffer</a>
</td>
<td align="left" width="63%">
Get a constant-buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1039fad-bd3d-406b-a2b4-6e8abc0381af">GetTextureBuffer</a>
</td>
<td align="left" width="63%">
Get a texture-buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65950d1c-b41f-45d9-94fc-16a87aebb0ad">SetConstantBuffer</a>
</td>
<td align="left" width="63%">
Set a constant-buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eee7b7b5-02e4-420e-a7f2-95259846f749">SetTextureBuffer</a>
</td>
<td align="left" width="63%">
Set a texture-buffer.

</td>
</tr>
</table> 


## -remarks



Use constant buffers to store many effect constants; grouping constants into buffers based on their frequency of update. This allows you to minimize the number of state changes as well as make the fewest API calls to change state. Both of these factors lead to better performance.




## -see-also




<a href="https://msdn.microsoft.com/ebe0afc7-6261-4c96-a54e-9b491e240c03">Effect Interfaces (Direct3D 10)</a>



<a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable</a>
 

 

