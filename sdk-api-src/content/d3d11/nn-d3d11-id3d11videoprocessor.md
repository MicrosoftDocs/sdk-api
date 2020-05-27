---
UID: NN:d3d11.ID3D11VideoProcessor
title: ID3D11VideoProcessor (d3d11.h)
description: Represents a video processor for Microsoft Direct3D 11.
helpviewer_keywords: ["ID3D11VideoProcessor","ID3D11VideoProcessor interface [Media Foundation]","ID3D11VideoProcessor interface [Media Foundation]","described","d3d11/ID3D11VideoProcessor","mf.id3d11videoprocessor"]
old-location: mf\id3d11videoprocessor.htm
tech.root: medfound
ms.assetid: AF6F6781-A7F9-4196-8E91-FDFDD1924E24
ms.date: 12/05/2018
ms.keywords: ID3D11VideoProcessor, ID3D11VideoProcessor interface [Media Foundation], ID3D11VideoProcessor interface [Media Foundation],described, d3d11/ID3D11VideoProcessor, mf.id3d11videoprocessor
f1_keywords:
- d3d11/ID3D11VideoProcessor
dev_langs:
- c++
req.header: d3d11.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d3d11.h
api_name:
- ID3D11VideoProcessor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoProcessor interface


## -description


Represents a video processor for Microsoft Direct3D 11.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoProcessor</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11VideoProcessor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11VideoProcessor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessor-getcontentdesc">GetContentDesc</a>
</td>
<td align="left" width="63%">
Gets the content description that was used to create the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessor-getrateconversioncaps">GetRateConversionCaps</a>
</td>
<td align="left" width="63%">
Gets the rate conversion capabilities of the video processor.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-interfaces">Direct3D 11 Video Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>
 

 

