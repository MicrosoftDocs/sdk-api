---
UID: NN:d3d11sdklayers.ID3D11RefDefaultTrackingOptions
title: ID3D11RefDefaultTrackingOptions (d3d11sdklayers.h)
description: The default tracking interface sets reference default tracking options.
helpviewer_keywords: ["ID3D11RefDefaultTrackingOptions","ID3D11RefDefaultTrackingOptions interface [Direct3D 11]","ID3D11RefDefaultTrackingOptions interface [Direct3D 11]","described","d3d11sdklayers/ID3D11RefDefaultTrackingOptions","direct3d11.id3d11refdefaulttrackingoptions"]
old-location: direct3d11\id3d11refdefaulttrackingoptions.htm
tech.root: direct3d11
ms.assetid: B6DD9810-275E-466B-8FE8-64EED0933B45
ms.date: 12/05/2018
ms.keywords: ID3D11RefDefaultTrackingOptions, ID3D11RefDefaultTrackingOptions interface [Direct3D 11], ID3D11RefDefaultTrackingOptions interface [Direct3D 11],described, d3d11sdklayers/ID3D11RefDefaultTrackingOptions, direct3d11.id3d11refdefaulttrackingoptions
req.header: d3d11sdklayers.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3DCompiler.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11RefDefaultTrackingOptions
 - d3d11sdklayers/ID3D11RefDefaultTrackingOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler.lib
 - D3DCompiler.dll
api_name:
 - ID3D11RefDefaultTrackingOptions
---

# ID3D11RefDefaultTrackingOptions interface


## -description

The default tracking interface sets reference default tracking options.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11RefDefaultTrackingOptions</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11RefDefaultTrackingOptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11RefDefaultTrackingOptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11refdefaulttrackingoptions-settrackingoptions">SetTrackingOptions</a>
</td>
<td align="left" width="63%">
Sets GPU debug reference default tracking options for specific resource types.
      

</td>
</tr>
</table>

## -remarks

These APIs require the Windows Software Development Kit (SDK) for Windows 8.

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-layer-interfaces">Layer Interfaces</a>