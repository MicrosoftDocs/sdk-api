---
UID: NN:sbtsv.ITsSbResourceNotificationEx
title: ITsSbResourceNotificationEx (sbtsv.h)
author: windows-sdk-content
description: Exposes methods that Remote Desktop Connection Broker (RD Connection Broker) uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.
old-location: termserv\itssbresourcenotificationex.htm
tech.root: TermServ
ms.assetid: 5e40535d-62b2-4d16-a995-61c24aefb2e5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITsSbResourceNotificationEx, ITsSbResourceNotificationEx interface [Remote Desktop Services], ITsSbResourceNotificationEx interface [Remote Desktop Services],described, sbtsv/ITsSbResourceNotificationEx, termserv.itssbresourcenotificationex
ms.topic: interface
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
 - ITsSbResourceNotificationEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbResourceNotificationEx interface


## -description


Exposes methods that Remote Desktop Connection Broker (RD Connection Broker) uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects. Plug-ins can use these notifications in many ways. For example, they can implement load-balancing algorithms.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbResourceNotificationEx</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbResourceNotificationEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbResourceNotificationEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcenotificationex-notifyclientconnectionstatechangeex">NotifyClientConnectionStateChangeEx</a>
</td>
<td align="left" width="63%">
Notifies registered plug-ins about state changes in a client connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcenotificationex-notifysessionchangeex">NotifySessionChangeEx</a>
</td>
<td align="left" width="63%">
Notifies registered plug-ins about state changes in a session object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcenotificationex-notifytargetchangeex">NotifyTargetChangeEx</a>
</td>
<td align="left" width="63%">
Notifies registered plug-ins about state changes in a target object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification">ITsSbResourceNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
 

 

