---
UID: NN:sbtsv.ITsSbResourceNotification
title: ITsSbResourceNotification
author: windows-sdk-content
description: Exposes methods that Remote Desktop Connection Broker (RD Connection Broker) uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.
old-location: termserv\itssbresourcenotification.htm
tech.root: termserv
ms.assetid: 70785b82-239d-4957-9703-ced685a2e0b8
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITsSbResourceNotification, ITsSbResourceNotification interface [Remote Desktop Services], ITsSbResourceNotification interface [Remote Desktop Services],described, sbtsv/ITsSbResourceNotification, termserv.itssbresourcenotification
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITsSbResourceNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbResourceNotification interface


## -description


Exposes methods that Remote Desktop Connection Broker (RD Connection Broker) uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects. Plug-ins can use these notifications in many ways. For example, they can implement load-balancing algorithms.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbResourceNotification</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITsSbResourceNotification</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbResourceNotification</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c5d6cf4-f99c-46fa-8b8e-008ff8a4d0d7">NotifyClientConnectionStateChange</a>
</td>
<td align="left" width="63%">
Notifies registered plug-ins about state changes in a client connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1efe806-a448-42d7-8bcd-bd763c00c732">NotifySessionChange</a>
</td>
<td align="left" width="63%">
Notifies registered plug-ins about state changes in a session object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d075c7ae-fe86-4547-a980-2b82ea3498c6">NotifyTargetChange</a>
</td>
<td align="left" width="63%">
Notifies registered plug-ins about state changes in a target object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5e40535d-62b2-4d16-a995-61c24aefb2e5">ITsSbResourceNotificationEx</a>



<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

