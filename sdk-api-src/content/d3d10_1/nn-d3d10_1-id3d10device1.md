---
UID: NN:d3d10_1.ID3D10Device1
title: ID3D10Device1
author: windows-sdk-content
description: The device interface represents a virtual adapter for Direct3D 10.1; it is used to perform rendering and create Direct3D resources.
old-location: direct3d10\id3d10device1.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device1.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID3D10Device1, ID3D10Device1 interface [Direct3D 10], ID3D10Device1 interface [Direct3D 10],described, a168edcd-989a-13da-7972-09b5d5e9210a, d3d10_1/ID3D10Device1, direct3d10.id3d10device1
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
 - ID3D10Device1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device1 interface


## -description


The device interface represents a virtual adapter for Direct3D 10.1; it is used to perform rendering and create Direct3D resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Device1</b> interface inherits from <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>. <b>ID3D10Device1</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b1f013f6-ab97-4b87-84df-7391482535bd">CreateBlendState1</a>
</td>
<td align="left" width="63%">
Create a blend-state object that encapsules blend state for the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10a2ffe7-fb5b-4ba9-8b61-5a37b901b514">CreateShaderResourceView1</a>
</td>
<td align="left" width="63%">
Create a shader-resource <a href="https://msdn.microsoft.com/ccfe6273-0dcf-4b42-9d74-665a0b4cd14a">view</a> for accessing data in a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecf697eb-06d7-488b-a59c-dfd3c2431353">GetFeatureLevel</a>
</td>
<td align="left" width="63%">
Gets the feature level of the hardware device.

</td>
</tr>
</table> 


## -remarks



A device is created using <a href="https://msdn.microsoft.com/6eed32f7-985e-4456-815e-d289acba7ae7">D3D10CreateDevice1</a>.

This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/f5ad2db8-da90-4bcd-83a7-7466723a9c3c">Core Interfaces</a>



<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>
 

 

