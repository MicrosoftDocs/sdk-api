---
UID: NN:wdstptmgmt.IWdsTransportNamespaceScheduledCast
title: IWdsTransportNamespaceScheduledCast (wdstptmgmt.h)
author: windows-sdk-content
description: Represents a base interface to the derived interfaces:\_IWdsTransportNamespaceScheduledCastManualStart and IWdsTransportNamespaceScheduledCastAutoStart.
old-location: wds\iwdstransportnamespacescheduledcast.htm
tech.root: wds
ms.assetid: 434e2eb2-b149-46e6-b7d0-0d07c44bcec2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWdsTransportNamespaceScheduledCast, IWdsTransportNamespaceScheduledCast interface [Windows Deployment Services], IWdsTransportNamespaceScheduledCast interface [Windows Deployment Services],described, wds.iwdstransportnamespacescheduledcast, wdstptmgmt/IWdsTransportNamespaceScheduledCast
ms.topic: interface
f1_keywords: 
 - "wdstptmgmt/IWdsTransportNamespaceScheduledCast"
dev_langs:
 - c++
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wdstptmgmt.tlb
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportNamespaceScheduledCast
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWdsTransportNamespaceScheduledCast interface


## -description


Represents a base interface to the derived interfaces: <a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespacescheduledcastmanualstart">IWdsTransportNamespaceScheduledCastManualStart</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespacescheduledcastautostart">IWdsTransportNamespaceScheduledCastAutoStart</a>. An administrator must start  multicast sessions that are hosted by a namespace object of  these derived interfaces.   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportNamespaceScheduledCast</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a>. <b>IWdsTransportNamespaceScheduledCast</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWdsTransportNamespaceScheduledCast</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespacescheduledcast-starttransmission">StartTransmission</a>
</td>
<td align="left" width="63%">
Starts a transmission on a namespace.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a>
 

 

