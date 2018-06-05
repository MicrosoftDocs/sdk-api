---
UID: NN:d3d10effect.ID3D10EffectSamplerVariable
title: ID3D10EffectSamplerVariable
author: windows-sdk-content
description: A sampler interface accesses sampler state.
old-location: direct3d10\id3d10effectsamplervariable.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectsamplervariable.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 5f4e0586-ee65-dc10-114c-2c07af8387a7, ID3D10EffectSamplerVariable, ID3D10EffectSamplerVariable interface [Direct3D 10], ID3D10EffectSamplerVariable interface [Direct3D 10],described, d3d10effect/ID3D10EffectSamplerVariable, direct3d10.id3d10effectsamplervariable
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10EffectSamplerVariable
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10EffectSamplerVariable interface


## -description


A sampler interface accesses sampler state.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10EffectSamplerVariable</b> interface inherits from <a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable</a>. <b>ID3D10EffectSamplerVariable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10EffectSamplerVariable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cb808d6-fa2b-4268-ae24-c295bf3e0b6c">GetBackingStore</a>
</td>
<td align="left" width="63%">
Get a pointer to a variable that contains sampler state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e3af04f-d5ea-455b-a950-c5929fa61409">GetSampler</a>
</td>
<td align="left" width="63%">
Get a pointer to a sampler interface.

</td>
</tr>
</table> 


## -remarks



An <b>ID3D10EffectSamplerVariable Interface</b> is created when an effect is read into memory.

Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device. You
 can use either of these methods to return state. For examples, see <a href="https://msdn.microsoft.com/743261a8-fdd8-492e-be8a-4faeb9b6f986">Two Ways to Get the State in an Effect Variable</a>.




## -see-also




<a href="https://msdn.microsoft.com/ebe0afc7-6261-4c96-a54e-9b491e240c03">Effect Interfaces (Direct3D 10)</a>



<a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable</a>
 

 

