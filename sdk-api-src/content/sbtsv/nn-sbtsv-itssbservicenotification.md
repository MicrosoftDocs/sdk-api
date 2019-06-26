---
UID: NN:sbtsv.ITsSbServiceNotification
title: ITsSbServiceNotification (sbtsv.h)
author: windows-sdk-content
description: Exposes methods that Remote Desktop Connection Broker (RD Connection Broker) uses to notify plug-ins of state changes that occur in the RD Connection Broker itself.
old-location: termserv\itssbservicenotification.htm
tech.root: TermServ
ms.assetid: 19b90ada-5277-47cb-a8d5-18f5c89612c0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITsSbServiceNotification, ITsSbServiceNotification interface [Remote Desktop Services], ITsSbServiceNotification interface [Remote Desktop Services],described, sbtsv/ITsSbServiceNotification, termserv.itssbservicenotification
ms.topic: interface
f1_keywords: 
 - "sbtsv/ITsSbServiceNotification"
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - sbtsv.h
api_name:
 - ITsSbServiceNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbServiceNotification interface


## -description


Exposes methods that Remote Desktop Connection Broker (RD Connection Broker) uses to notify plug-ins of state changes that occur in the RD Connection Broker itself.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbServiceNotification</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbServiceNotification</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbServiceNotification</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbservicenotification-notifyservicefailure">NotifyServiceFailure</a>
</td>
<td align="left" width="63%">
Notifies registered plug-ins that the RD Connection Broker service has stopped.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbservicenotification-notifyservicesuccess">NotifyServiceSuccess</a>
</td>
<td align="left" width="63%">
Notifies registered plug-ins that the RD Connection Broker service has started.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
 

 

