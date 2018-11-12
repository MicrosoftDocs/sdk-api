---
UID: NN:d3d11.ID3D11VideoProcessor
title: ID3D11VideoProcessor
author: windows-sdk-content
description: Represents a video processor for Microsoft Direct3D 11.
old-location: mf\id3d11videoprocessor.htm
tech.root: medfound
ms.assetid: AF6F6781-A7F9-4196-8E91-FDFDD1924E24
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ID3D11VideoProcessor, ID3D11VideoProcessor interface [Media Foundation], ID3D11VideoProcessor interface [Media Foundation],described, d3d11/ID3D11VideoProcessor, mf.id3d11videoprocessor
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
 - ID3D11VideoProcessor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoProcessor interface


## -description


Represents a video processor for Microsoft Direct3D 11.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoProcessor</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>. <b>ID3D11VideoProcessor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8C8433BC-1DB9-45D9-817A-7175B4577818">GetContentDesc</a>
</td>
<td align="left" width="63%">
Gets the content description that was used to create the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CC1ED2C7-8277-4F2A-801D-7534CE383DAD">GetRateConversionCaps</a>
</td>
<td align="left" width="63%">
Gets the rate conversion capabilities of the video processor.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/en-us/library/Hh447788(v=VS.85).aspx">ID3D11VideoDevice::CreateVideoProcessor</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447679(v=VS.85).aspx">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>
 

 

