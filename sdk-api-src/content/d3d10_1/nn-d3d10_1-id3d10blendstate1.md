---
UID: NN:d3d10_1.ID3D10BlendState1
title: ID3D10BlendState1
author: windows-sdk-content
description: This blend-state interface accesses blending state for a Direct3D 10.1 device for the output-merger stage.
old-location: direct3d10\id3d10blendstate1.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10blendstate1.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 50959f42-4209-b827-553e-862c94c85dfc, ID3D10BlendState1, ID3D10BlendState1 interface [Direct3D 10], ID3D10BlendState1 interface [Direct3D 10],described, d3d10_1/ID3D10BlendState1, direct3d10.id3d10blendstate1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d10_1.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10BlendState1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10BlendState1 interface


## -description


This blend-state interface accesses blending state for a Direct3D 10.1 device for the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger</a> stage.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10BlendState1</b> interface inherits from <a href="https://msdn.microsoft.com/fe0186f5-cd8f-478d-9009-a0f82830cd1f">ID3D10BlendState</a>. <b>ID3D10BlendState1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10BlendState1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/edddc555-47f2-4baa-8312-8ececafca07a">GetDesc</a>
</td>
<td align="left" width="63%">
Get the blend state.

</td>
</tr>
</table> 


## -remarks



Blending combines two pixel values. You have control over how the pixels are blended by using a predefined set of blending operations, as well as preblending operations. The <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">Blending Block Diagram</a> shows conceptually how blending works.

To create a blend-state interface, call <a href="https://msdn.microsoft.com/b1f013f6-ab97-4b87-84df-7391482535bd">ID3D10Device1::CreateBlendState1</a>. To initialize the blend state, call <a href="https://msdn.microsoft.com/39169f4f-8a7b-4db0-abd5-5b67b204b394">ID3D10Device::OMSetBlendState</a>.

This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/f5ad2db8-da90-4bcd-83a7-7466723a9c3c">Core Interfaces</a>



<a href="https://msdn.microsoft.com/fe0186f5-cd8f-478d-9009-a0f82830cd1f">ID3D10BlendState</a>
 

 

