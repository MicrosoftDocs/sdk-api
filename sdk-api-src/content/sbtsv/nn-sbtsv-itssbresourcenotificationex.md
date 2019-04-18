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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbResourceNotificationEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITsSbResourceNotificationEx</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/79f59e18-f9ca-4e64-b8a1-8b0dd2b2715e">NotifyClientConnectionStateChangeEx</a>
</td>
<td align="left" width="63%">
Notifies registered plug-ins about state changes in a client connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75f7371a-fd3e-4045-b8fe-23d57d75b27a">NotifySessionChangeEx</a>
</td>
<td align="left" width="63%">
Notifies registered plug-ins about state changes in a session object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f1f07ce-4b5d-4e21-834d-f554bd73cc63">NotifyTargetChangeEx</a>
</td>
<td align="left" width="63%">
Notifies registered plug-ins about state changes in a target object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/70785b82-239d-4957-9703-ced685a2e0b8">ITsSbResourceNotification</a>



<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

