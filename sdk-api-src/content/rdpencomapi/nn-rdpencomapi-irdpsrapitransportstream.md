---
UID: NN:rdpencomapi.IRDPSRAPITransportStream
title: IRDPSRAPITransportStream (rdpencomapi.h)
description: Exposes methods that perform operations with streams.helpviewer_keywords: ["IRDPSRAPITransportStream","IRDPSRAPITransportStream interface [RDP]","IRDPSRAPITransportStream interface [RDP]","described","rdp.irdpsrapitransportstream","rdpencomapi/IRDPSRAPITransportStream"]
old-location: rdp\irdpsrapitransportstream.htm
tech.root: rdp
ms.assetid: 18ac00d5-f574-463f-a34a-40c2dc16d4d8
ms.date: 12/05/2018
ms.keywords: IRDPSRAPITransportStream, IRDPSRAPITransportStream interface [RDP], IRDPSRAPITransportStream interface [RDP],described, rdp.irdpsrapitransportstream, rdpencomapi/IRDPSRAPITransportStream
f1_keywords:
- rdpencomapi/IRDPSRAPITransportStream
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRDPSRAPITransportStream interface


## -description


Exposes methods that perform operations with streams.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPITransportStream</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRDPSRAPITransportStream</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapitransportstream-allocbuffer">AllocBuffer</a>
</td>
<td align="left" width="63%">
Called by the Remote Desktop Protocol (RDP) stack to allocate a stream buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapitransportstream-close">Close</a>
</td>
<td align="left" width="63%">
Called by the RDP stack to close the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapitransportstream-freebuffer">FreeBuffer</a>
</td>
<td align="left" width="63%">
Called by the RDP stack to return a stream buffer to the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapitransportstream-open">Open</a>
</td>
<td align="left" width="63%">
Called by the RDP stack to start the stream and indicate that the RDP stack is ready to receive notifications of events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapitransportstream-readbuffer">ReadBuffer</a>
</td>
<td align="left" width="63%">
Called by the RDP stack to read the contents of a stream buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapitransportstream-writebuffer">WriteBuffer</a>
</td>
<td align="left" width="63%">
Called by the RDP stack to write the contents of a stream buffer to the network.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreambuffer">IRDPSRAPITransportStreamBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreamevents">IRDPSRAPITransportStreamEvents</a>
 

 

