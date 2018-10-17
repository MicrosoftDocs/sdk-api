---
UID: NN:d3d11.ID3D11VideoDecoderOutputView
title: ID3D11VideoDecoderOutputView
author: windows-sdk-content
description: Identifies the output surfaces that can be accessed during video decoding.
old-location: mf\id3d11videodecoderoutputview.htm
tech.root: medfound
ms.assetid: 389E0CCC-4DD2-4E82-84D7-3794AEE59208
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ID3D11VideoDecoderOutputView, ID3D11VideoDecoderOutputView interface [Media Foundation], ID3D11VideoDecoderOutputView interface [Media Foundation],described, d3d11/ID3D11VideoDecoderOutputView, mf.id3d11videodecoderoutputview
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ID3D11VideoDecoderOutputView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoDecoderOutputView interface


## -description


Identifies the output surfaces that can be accessed during video decoding.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoDecoderOutputView</b> interface inherits from <a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a>. <b>ID3D11VideoDecoderOutputView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11VideoDecoderOutputView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/002BE600-2B4C-4337-BAA4-EC132FD3BC8A">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the properties of the video decoder output view.


</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/8A3D72CF-B641-4219-8C88-FCE5231CF2F6">ID3D11VideoDevice::CreateVideoDecoderOutputView</a>.




## -see-also




<a href="https://msdn.microsoft.com/2AE97FFE-0FA4-4CC0-8433-7BA46BCACE30">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a>
 

 

