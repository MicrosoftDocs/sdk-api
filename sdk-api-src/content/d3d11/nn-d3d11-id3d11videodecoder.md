---
UID: NN:d3d11.ID3D11VideoDecoder
title: ID3D11VideoDecoder
author: windows-sdk-content
description: Represents a hardware-accelerated video decoder for Microsoft Direct3D 11.
old-location: mf\id3d11videodecoder.htm
tech.root: medfound
ms.assetid: F25AFA0B-7413-40F0-AFF8-C9B4549305D2
ms.author: windowssdkdev
ms.date: 10/05/2018
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoDecoder</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>. <b>ID3D11VideoDecoder</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Hh447769(v=VS.85).aspx">GetCreationParameters</a>
</td>
<td align="left" width="63%">
Gets the parameters that were used to create the decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447780(v=VS.85).aspx">GetDriverHandle</a>
</td>
<td align="left" width="63%">
Gets a handle to the driver.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/en-us/library/Hh447786(v=VS.85).aspx">ID3D11VideoDevice::CreateVideoDecoder</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447679(v=VS.85).aspx">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>
 

 

