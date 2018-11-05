---
UID: NN:d3d11.ID3D11AuthenticatedChannel
title: ID3D11AuthenticatedChannel
author: windows-sdk-content
description: Provides a communication channel with the graphics driver or the Microsoft Direct3D runtime.
old-location: mf\id3d11authenticatedchannel.htm
tech.root: medfound
ms.assetid: B2DE8E06-1571-4D50-9296-8EB4BB74D6BA
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ID3D11AuthenticatedChannel, ID3D11AuthenticatedChannel interface [Media Foundation], ID3D11AuthenticatedChannel interface [Media Foundation],described, d3d11/ID3D11AuthenticatedChannel, mf.id3d11authenticatedchannel
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
 - ID3D11AuthenticatedChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11AuthenticatedChannel interface


## -description


Provides a communication channel with the graphics driver or the Microsoft Direct3D runtime.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11AuthenticatedChannel</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11AuthenticatedChannel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11AuthenticatedChannel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D7FC07CA-B045-4C44-B3FD-B902C5437E47">GetCertificate</a>
</td>
<td align="left" width="63%">
Gets the driver's certificate chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B393140A-9744-4290-B168-4E7F4E9F55DC">GetCertificateSize</a>
</td>
<td align="left" width="63%">
Gets the size of the driver's certificate chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CA32D01B-B0B7-4F4F-8F48-747448DEC735">GetChannelHandle</a>
</td>
<td align="left" width="63%">
Gets a handle to the authenticated channel.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/4325E83F-23BF-4104-B30E-27DBE7D23D88">ID3D11VideoDevice::CreateAuthenticatedChannel</a>.




## -see-also




<a href="https://msdn.microsoft.com/2AE97FFE-0FA4-4CC0-8433-7BA46BCACE30">Direct3D 11 Video Interfaces</a>
 

 

