---
UID: NN:rdpencomapi.IRDPSRAPITransportStreamEvents
title: IRDPSRAPITransportStreamEvents (rdpencomapi.h)
author: windows-sdk-content
description: Exposes methods called by the stream interface (IRDPSRAPITransportStream) to notify the Remote Desktop Protocol (RDP) stack about the completion of events.
old-location: rdp\irdpsrapitransportstreamevents.htm
tech.root: rdp
ms.assetid: d38ee3fb-3867-40c9-8e6a-35c94762fdf4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRDPSRAPITransportStreamEvents, IRDPSRAPITransportStreamEvents interface [RDP], IRDPSRAPITransportStreamEvents interface [RDP],described, rdp.irdpsrapitransportstreamevents, rdpencomapi/IRDPSRAPITransportStreamEvents
ms.topic: interface
f1_keywords: 
 - "rdpencomapi/IRDPSRAPITransportStreamEvents"
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
 - IRDPSRAPITransportStreamEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRDPSRAPITransportStreamEvents interface


## -description


Exposes methods called by the  stream interface (<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstream">IRDPSRAPITransportStream</a>) to notify the Remote Desktop Protocol (RDP) stack about the completion of events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPITransportStreamEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRDPSRAPITransportStreamEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRDPSRAPITransportStreamEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapitransportstreamevents-onreadcompleted">OnReadCompleted</a>
</td>
<td align="left" width="63%">
Notifies the RDP stack that a read operation has completed. The RDP stack resumes ownership of the stream buffer and uses it for subsequent operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapitransportstreamevents-onstreamclosed">OnStreamClosed</a>
</td>
<td align="left" width="63%">
Notifies the RDP stack that the connection was closed. If an error occurred, the stream interface should provide a return value that specifies which error occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapitransportstreamevents-onwritecompleted">OnWriteCompleted</a>
</td>
<td align="left" width="63%">
Notifies the RDP stack that a write operation has completed. The RDP stack resumes ownership of the stream buffer and uses it for subsequent operations.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstream">IRDPSRAPITransportStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreambuffer">IRDPSRAPITransportStreamBuffer</a>
 

 

