---
UID: NN:d3d11.ID3D11VideoDecoder
title: ID3D11VideoDecoder
author: windows-sdk-content
description: Represents a hardware-accelerated video decoder for Microsoft Direct3D 11.
old-location: mf\id3d11videodecoder.htm
tech.root: medfound
ms.assetid: F25AFA0B-7413-40F0-AFF8-C9B4549305D2
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ID3D11VideoDecoder, ID3D11VideoDecoder interface [Media Foundation], ID3D11VideoDecoder interface [Media Foundation],described, d3d11/ID3D11VideoDecoder, mf.id3d11videodecoder
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
 - ID3D11VideoDecoder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoDecoder interface


## -description


Represents a hardware-accelerated video decoder for Microsoft Direct3D 11.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoDecoder</b> interface inherits from <a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>. <b>ID3D11VideoDecoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11VideoDecoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6F104317-19C2-4FCB-8CA7-34FD0C237822">GetCreationParameters</a>
</td>
<td align="left" width="63%">
Gets the parameters that were used to create the decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CD9A46DB-C16D-4DF4-972B-2CE8398CEE98">GetDriverHandle</a>
</td>
<td align="left" width="63%">
Gets a handle to the driver.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/7EC2C7C3-F2EB-4357-BD53-308ABFFC9BE8">ID3D11VideoDevice::CreateVideoDecoder</a>.




## -see-also




<a href="https://msdn.microsoft.com/2AE97FFE-0FA4-4CC0-8433-7BA46BCACE30">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>
 

 

