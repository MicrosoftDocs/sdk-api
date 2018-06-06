---
UID: NN:d3d10effect.ID3D10EffectPool
title: ID3D10EffectPool
author: windows-sdk-content
description: A pool interface represents a common memory space (or pool) for sharing variables between effects.
old-location: direct3d10\id3d10effectpool.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectpool.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 3c4865e5-4958-111b-ced6-75e2e367d986, ID3D10EffectPool, ID3D10EffectPool interface [Direct3D 10], ID3D10EffectPool interface [Direct3D 10],described, d3d10effect/ID3D10EffectPool, direct3d10.id3d10effectpool
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d10effect.h
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
 - ID3D10EffectPool
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10EffectPool interface


## -description


A pool interface represents a common memory space (or pool) for sharing variables between effects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10EffectPool</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D10EffectPool</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10EffectPool</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58622696-943f-4355-b6d4-f243216c8649">AsEffect</a>
</td>
<td align="left" width="63%">
Get the effect that created the effect pool.

</td>
</tr>
</table> 


## -remarks



To create an effect pool, call a function like <a href="https://msdn.microsoft.com/be738374-a91e-43d3-9cec-14882e6317ee">D3DX10CreateEffectPoolFromFile</a>. Effect pools can improve performance by reducing the number of API calls required to make state changes (see <a href="https://msdn.microsoft.com/9f029be5-4ce0-46ca-909b-adaa980398e7">Using Effect Pools</a>).




## -see-also




<a href="https://msdn.microsoft.com/ebe0afc7-6261-4c96-a54e-9b491e240c03">Effect Interfaces (Direct3D 10)</a>
 

 

