---
UID: NN:sbtsv.ITsSbServiceNotification
title: ITsSbServiceNotification
author: windows-driver-content
description: Exposes methods that Remote Desktop Connection Broker (RD Connection Broker) uses to notify plug-ins of state changes that occur in the RD Connection Broker itself.
old-location: termserv\itssbservicenotification.htm
old-project: TermServ
ms.assetid: 19b90ada-5277-47cb-a8d5-18f5c89612c0
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITsSbServiceNotification, ITsSbServiceNotification interface [Remote Desktop Services], ITsSbServiceNotification interface [Remote Desktop Services],described, sbtsv/ITsSbServiceNotification, termserv.itssbservicenotification
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
req.typenames: TS_SB_SORT_BY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sbtsv.h
api_name:
-	ITsSbServiceNotification
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITsSbServiceNotification interface


## -description


Exposes methods that Remote Desktop Connection Broker (RD Connection Broker) uses to notify plug-ins of state changes that occur in the RD Connection Broker itself.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbServiceNotification</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITsSbServiceNotification</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/76e8819f-93d0-4f1b-a573-5b9aeaaae08a">NotifyServiceFailure</a>
</td>
<td align="left" width="63%">
Notifies registered plug-ins that the RD Connection Broker service has stopped.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/063ed950-f168-491c-85db-14f35741c129">NotifyServiceSuccess</a>
</td>
<td align="left" width="63%">
Notifies registered plug-ins that the RD Connection Broker service has started.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

