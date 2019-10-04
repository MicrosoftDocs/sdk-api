---
UID: NN:d3d10_1.ID3D10Device1
title: ID3D10Device1 (d3d10_1.h)
author: windows-sdk-content
description: The device interface represents a virtual adapter for Direct3D 10.1; it is used to perform rendering and create Direct3D resources.
old-location: direct3d10\id3d10device1.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device1.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D10Device1, ID3D10Device1 interface [Direct3D 10], ID3D10Device1 interface [Direct3D 10],described, a168edcd-989a-13da-7972-09b5d5e9210a, d3d10_1/ID3D10Device1, direct3d10.id3d10device1
ms.topic: interface
f1_keywords: 
 - "d3d10_1/ID3D10Device1"
dev_langs:
 - c++
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
 - ID3D10Device1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Device1 interface


## -description


The device interface represents a virtual adapter for Direct3D 10.1; it is used to perform rendering and create Direct3D resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Device1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>. <b>ID3D10Device1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10Device1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10_1/nf-d3d10_1-id3d10device1-createblendstate1">CreateBlendState1</a>
</td>
<td align="left" width="63%">
Create a blend-state object that encapsules blend state for the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10_1/nf-d3d10_1-id3d10device1-createshaderresourceview1">CreateShaderResourceView1</a>
</td>
<td align="left" width="63%">
Create a shader-resource <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">view</a> for accessing data in a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10_1/nf-d3d10_1-id3d10device1-getfeaturelevel">GetFeatureLevel</a>
</td>
<td align="left" width="63%">
Gets the feature level of the hardware device.

</td>
</tr>
</table> 


## -remarks



A device is created using <a href="https://docs.microsoft.com/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1">D3D10CreateDevice1</a>.

This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>
 

 

