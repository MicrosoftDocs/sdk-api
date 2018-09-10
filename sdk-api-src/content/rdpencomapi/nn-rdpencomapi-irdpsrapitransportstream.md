---
UID: NN:rdpencomapi.IRDPSRAPITransportStream
title: IRDPSRAPITransportStream
author: windows-sdk-content
description: Exposes methods that perform operations with streams.
old-location: rdp\irdpsrapitransportstream.htm
tech.root: Rdp
ms.assetid: 18ac00d5-f574-463f-a34a-40c2dc16d4d8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IRDPSRAPITransportStream, IRDPSRAPITransportStream interface [RDP], IRDPSRAPITransportStream interface [RDP],described, rdp.irdpsrapitransportstream, rdpencomapi/IRDPSRAPITransportStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPITransportStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPSRAPITransportStream interface


## -description


Exposes methods that perform operations with streams.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPITransportStream</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRDPSRAPITransportStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRDPSRAPITransportStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e53aedb-d3a2-4468-9df9-f058485d7bc4">AllocBuffer</a>
</td>
<td align="left" width="63%">
Called by the Remote Desktop Protocol (RDP) stack to allocate a stream buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c9ddc69-bc40-4c75-b4ff-3ff622dcf76c">Close</a>
</td>
<td align="left" width="63%">
Called by the RDP stack to close the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db2f0bc2-cddf-44bd-9899-192e5eb014bb">FreeBuffer</a>
</td>
<td align="left" width="63%">
Called by the RDP stack to return a stream buffer to the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55d53ed6-8046-4605-b543-ab0e5ad8d8f7">Open</a>
</td>
<td align="left" width="63%">
Called by the RDP stack to start the stream and indicate that the RDP stack is ready to receive notifications of events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a6d9a76-48b8-4755-985e-efbef01a6382">ReadBuffer</a>
</td>
<td align="left" width="63%">
Called by the RDP stack to read the contents of a stream buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e78360d-9ea6-4a74-8a20-5546057c24b0">WriteBuffer</a>
</td>
<td align="left" width="63%">
Called by the RDP stack to write the contents of a stream buffer to the network.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/44087315-7a71-4557-89b3-bf8c66ed10a4">IRDPSRAPITransportStreamBuffer</a>



<a href="https://msdn.microsoft.com/d38ee3fb-3867-40c9-8e6a-35c94762fdf4">IRDPSRAPITransportStreamEvents</a>
 

 

