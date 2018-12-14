---
UID: NN:d3d11_1.ID3D11VideoDevice1
title: ID3D11VideoDevice1
author: windows-sdk-content
description: Provides the video decoding and video processing capabilities of a Microsoft Direct3D 11 device.
old-location: mf\id3d11videodevice1.htm
tech.root: medfound
ms.assetid: 10E68945-6103-491D-8846-3B7C880FEAFD
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11VideoDevice1, ID3D11VideoDevice1 interface [Media Foundation], ID3D11VideoDevice1 interface [Media Foundation],described, d3d11_1/ID3D11VideoDevice1, mf.id3d11videodevice1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - ID3D11VideoDevice1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoDevice1 interface


## -description


Provides the video decoding and video processing capabilities of a Microsoft Direct3D 11 device. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoDevice1</b> interface inherits from <a href="https://msdn.microsoft.com/420DE3C4-15A9-4EEB-A1FD-6350DE109CFF">ID3D11VideoDevice</a>. <b>ID3D11VideoDevice1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/EB05C2F7-AC7A-42BD-A661-5101641A920C">CheckVideoDecoderDownsampling</a>
</td>
<td align="left" width="63%">
Indicates whether the video decoder supports downsampling with the specified input format, and whether real-time downsampling is supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3F973DA0-F722-4EC2-A578-F01B6999F16B">GetCryptoSessionPrivateDataSize</a>
</td>
<td align="left" width="63%">
Retrieves optional sizes for private driver data. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9F978BE5-568E-440C-B9B2-0972893FD970">GetVideoDecoderCaps</a>
</td>
<td align="left" width="63%">
Retrieves capabilities and limitations of the video decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DD1C1273-C069-4C46-933F-3450F9DDAFBD">RecommendVideoDecoderDownsampleParameters</a>
</td>
<td align="left" width="63%">
Allows the driver to recommend optimal output downsample parameters from the input parameters.

</td>
</tr>
</table> 


## -remarks



The Direct3D 11 device supports this interface. To get a pointer to this interface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> with an <a href="https://msdn.microsoft.com/DB4DAD13-3CD7-4362-950B-6403328CB071">ID3D11Device1</a> interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/2AE97FFE-0FA4-4CC0-8433-7BA46BCACE30">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>



<a href="https://msdn.microsoft.com/420DE3C4-15A9-4EEB-A1FD-6350DE109CFF">ID3D11VideoDevice</a>
 

 

