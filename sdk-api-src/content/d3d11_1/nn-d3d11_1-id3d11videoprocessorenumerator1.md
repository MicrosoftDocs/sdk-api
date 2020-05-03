---
UID: NN:d3d11_1.ID3D11VideoProcessorEnumerator1
title: ID3D11VideoProcessorEnumerator1 (d3d11_1.h)
description: Enumerates the video processor capabilities of a Microsoft Direct3D 11 device.helpviewer_keywords: ["ID3D11VideoProcessorEnumerator1","ID3D11VideoProcessorEnumerator1 interface [Media Foundation]","ID3D11VideoProcessorEnumerator1 interface [Media Foundation]","described","d3d11_1/ID3D11VideoProcessorEnumerator1","mf.id3d11videoprocessorenumerator1"]
old-location: mf\id3d11videoprocessorenumerator1.htm
tech.root: medfound
ms.assetid: BBC4C5BC-2DA0-48BD-B182-FBF62A2491A7
ms.date: 12/05/2018
ms.keywords: ID3D11VideoProcessorEnumerator1, ID3D11VideoProcessorEnumerator1 interface [Media Foundation], ID3D11VideoProcessorEnumerator1 interface [Media Foundation],described, d3d11_1/ID3D11VideoProcessorEnumerator1, mf.id3d11videoprocessorenumerator1
f1_keywords:
- d3d11_1/ID3D11VideoProcessorEnumerator1
dev_langs:
- c++
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
- d3d11_1.h
api_name:
- ID3D11VideoProcessorEnumerator1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoProcessorEnumerator1 interface


## -description


Enumerates the video processor capabilities of a Microsoft Direct3D 11 device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoProcessorEnumerator1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorenumerator">ID3D11VideoProcessorEnumerator</a>. <b>ID3D11VideoProcessorEnumerator1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11VideoProcessorEnumerator1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videoprocessorenumerator1-checkvideoprocessorformatconversion">CheckVideoProcessorFormatConversion</a>
</td>
<td align="left" width="63%">
Indicates whether the driver supports the specified combination of format and colorspace conversions.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorenumerator">ID3D11VideoDevice::CreateVideoProcessorEnumerator</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-interfaces">Direct3D 11 Video Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorenumerator">ID3D11VideoProcessorEnumerator</a>
 

 

