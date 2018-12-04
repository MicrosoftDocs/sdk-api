---
UID: NN:rdpencomapi.IRDPSRAPITransportStreamEvents
title: IRDPSRAPITransportStreamEvents
author: windows-sdk-content
description: Exposes methods called by the stream interface (IRDPSRAPITransportStream) to notify the Remote Desktop Protocol (RDP) stack about the completion of events.
old-location: rdp\irdpsrapitransportstreamevents.htm
tech.root: rdp
ms.assetid: d38ee3fb-3867-40c9-8e6a-35c94762fdf4
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IRDPSRAPITransportStreamEvents, IRDPSRAPITransportStreamEvents interface [RDP], IRDPSRAPITransportStreamEvents interface [RDP],described, rdp.irdpsrapitransportstreamevents, rdpencomapi/IRDPSRAPITransportStreamEvents
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IRDPSRAPITransportStreamEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPSRAPITransportStreamEvents interface


## -description


Exposes methods called by the  stream interface (<a href="https://msdn.microsoft.com/18ac00d5-f574-463f-a34a-40c2dc16d4d8">IRDPSRAPITransportStream</a>) to notify the Remote Desktop Protocol (RDP) stack about the completion of events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPITransportStreamEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRDPSRAPITransportStreamEvents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/27c3a16a-3d78-46b1-b328-1a1b6f059687">OnReadCompleted</a>
</td>
<td align="left" width="63%">
Notifies the RDP stack that a read operation has completed. The RDP stack resumes ownership of the stream buffer and uses it for subsequent operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98767b91-95c1-4883-b27c-16c20d1da507">OnStreamClosed</a>
</td>
<td align="left" width="63%">
Notifies the RDP stack that the connection was closed. If an error occurred, the stream interface should provide a return value that specifies which error occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19d99eba-e7ee-4bdc-8a9f-2cac97d17dea">OnWriteCompleted</a>
</td>
<td align="left" width="63%">
Notifies the RDP stack that a write operation has completed. The RDP stack resumes ownership of the stream buffer and uses it for subsequent operations.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/18ac00d5-f574-463f-a34a-40c2dc16d4d8">IRDPSRAPITransportStream</a>



<a href="https://msdn.microsoft.com/44087315-7a71-4557-89b3-bf8c66ed10a4">IRDPSRAPITransportStreamBuffer</a>
 

 

