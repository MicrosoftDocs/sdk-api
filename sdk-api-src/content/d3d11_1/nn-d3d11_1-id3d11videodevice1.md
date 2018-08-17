---
UID: NN:d3d11_1.ID3D11VideoDevice1
title: ID3D11VideoDevice1
author: windows-sdk-content
description: Provides the video decoding and video processing capabilities of a Microsoft Direct3D 11 device.
old-location: mf\id3d11videodevice1.htm
old-project: medfound
ms.assetid: 10E68945-6103-491D-8846-3B7C880FEAFD
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ID3D11VideoDevice1, ID3D11VideoDevice1 interface [Media Foundation], ID3D11VideoDevice1 interface [Media Foundation],described, d3d11_1/ID3D11VideoDevice1, mf.id3d11videodevice1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11_1.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_1.h
api_name:
 - ID3D11VideoDevice1
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11VideoDevice1 interface


## -description


Provides the video decoding and video processing capabilities of a Microsoft Direct3D 11 device. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoDevice1</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Hh447781(v=VS.85).aspx">ID3D11VideoDevice</a>. <b>ID3D11VideoDevice1</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11VideoDevice1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894142(v=VS.85).aspx">CheckVideoDecoderDownsampling</a>
</td>
<td align="left" width="63%">
Indicates whether the video decoder supports downsampling with the specified input format, and whether real-time downsampling is supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894143(v=VS.85).aspx">GetCryptoSessionPrivateDataSize</a>
</td>
<td align="left" width="63%">
Retrieves optional sizes for private driver data. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894144(v=VS.85).aspx">GetVideoDecoderCaps</a>
</td>
<td align="left" width="63%">
Retrieves capabilities and limitations of the video decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894145(v=VS.85).aspx">RecommendVideoDecoderDownsampleParameters</a>
</td>
<td align="left" width="63%">
Allows the driver to recommend optimal output downsample parameters from the input parameters.

</td>
</tr>
</table> 


## -remarks



The Direct3D 11 device supports this interface. To get a pointer to this interface, call <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> with an <a href="https://msdn.microsoft.com/en-us/library/Hh404575(v=VS.85).aspx">ID3D11Device1</a> interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447679(v=VS.85).aspx">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh447781(v=VS.85).aspx">ID3D11VideoDevice</a>
 

 

