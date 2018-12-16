---
UID: NN:d3d11_4.ID3D11VideoContext2
title: ID3D11VideoContext2
author: windows-sdk-content
description: Provides the video functionality of a Microsoft Direct3D 11 device.
old-location: mf\id3d11videocontext2.htm
tech.root: medfound
ms.assetid: E3FB5478-31CD-4AE3-BEA0-18823C4A4D3E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11VideoContext2, ID3D11VideoContext2 interface [Media Foundation], ID3D11VideoContext2 interface [Media Foundation],described, d3d11_4/ID3D11VideoContext2, mf.id3d11videocontext2, mf.id3dvideocontext2
ms.topic: interface
req.header: d3d11_4.h
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
 - d3d11_4.h
api_name:
 - ID3D11VideoContext2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext2 interface


## -description


Provides the video functionality of a Microsoft Direct3D 11 device. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoContext2</b> interface inherits from <a href="https://msdn.microsoft.com/64D12F68-C2AA-4C1D-9608-5F97CF7AD430">ID3D11VideoContext1</a>. <b>ID3D11VideoContext2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11VideoContext2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5739668F-DCF8-448C-8690-E254315B92AF">VideoProcessorGetOutputHDRMetaData</a>
</td>
<td align="left" width="63%">
Gets the HDR metadata describing the display on which the content will be presented. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08464EB5-8E1F-4E4B-A545-A18C82A0C921">VideoProcessorGetStreamHDRMetaData</a>
</td>
<td align="left" width="63%">
Gets the HDR metadata associated with the video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5905E3F2-B0A3-4FF6-B498-BC24BFD3F58F">VideoProcessorSetOutputHDRMetaData</a>
</td>
<td align="left" width="63%">
Sets the HDR metadata describing the display on which the content will be presented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C76CD8EF-3FBF-48B5-9633-BB65840BE34F">VideoProcessorSetStreamHDRMetaData</a>
</td>
<td align="left" width="63%">
Sets the HDR metadata associated with the video stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/64D12F68-C2AA-4C1D-9608-5F97CF7AD430">ID3D11VideoContext1</a>
 

 

