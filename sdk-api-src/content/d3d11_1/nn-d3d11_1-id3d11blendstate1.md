---
UID: NN:d3d11_1.ID3D11BlendState1
title: ID3D11BlendState1
author: windows-sdk-content
description: The blend-state interface holds a description for blending state that you can bind to the output-merger stage. This blend-state interface supports logical operations as well as blending operations.
old-location: direct3d11\id3d11blendstate1.htm
tech.root: direct3d11
ms.assetid: 5562F0B2-77FC-4614-BFA9-077323D4A2FA
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11BlendState1, ID3D11BlendState1 interface [Direct3D 11], ID3D11BlendState1 interface [Direct3D 11],described, d3d11_1/ID3D11BlendState1, direct3d11.id3d11blendstate1
ms.topic: interface
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11BlendState1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11BlendState1 interface


## -description


The blend-state interface holds a description for blending state that you can bind to the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a>. This blend-state interface supports logical operations as well as blending operations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11BlendState1</b> interface inherits from <a href="https://msdn.microsoft.com/ccb39c89-eba7-473c-8358-dc3513da4be7">ID3D11BlendState</a>. <b>ID3D11BlendState1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11BlendState1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BD256EB6-2FDD-4BBA-99E7-D7AA2CBDD629">GetDesc1</a>
</td>
<td align="left" width="63%">
Gets the description for blending state that you used to create the blend-state object.

</td>
</tr>
</table> 


## -remarks



Blending applies a simple function to combine output values from a pixel shader with data in a render target. You have control over how the pixels are blended by using a predefined set of blending operations and preblending operations.

To create a blend-state object, call <a href="https://msdn.microsoft.com/2E891104-3706-46A5-88FB-C621C95B4EFB">ID3D11Device1::CreateBlendState1</a>. To bind the blend-state object to the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a>, call <a href="https://msdn.microsoft.com/fabcae1d-2ad8-4f4d-8eef-18945e369225">ID3D11DeviceContext::OMSetBlendState</a>.




## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/ccb39c89-eba7-473c-8358-dc3513da4be7">ID3D11BlendState</a>
 

 

