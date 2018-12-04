---
UID: NN:sbtsv.ITsSbLoadBalancingNotifySink
title: ITsSbLoadBalancingNotifySink
author: windows-sdk-content
description: Exposes methods that return the result of a load-balancing algorithm to Remote Desktop Connection Broker (RD Connection Broker).
old-location: termserv\itssbloadbalancingnotifysink.htm
tech.root: termserv
ms.assetid: cc6d2616-27e1-4731-91bf-fe96bcea2cab
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ITsSbLoadBalancingNotifySink, ITsSbLoadBalancingNotifySink interface [Remote Desktop Services], ITsSbLoadBalancingNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbLoadBalancingNotifySink, termserv.itssbloadbalancingnotifysink
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
 - ITsSbLoadBalancingNotifySink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbLoadBalancingNotifySink interface


## -description


Exposes methods that return the result of a load-balancing algorithm to Remote Desktop Connection Broker (RD Connection Broker).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbLoadBalancingNotifySink</b> interface inherits from <a href="https://msdn.microsoft.com/11ef1bd4-301f-456b-a68b-2f32b75ac5ae">ITsSbBaseNotifySink</a>. <b>ITsSbLoadBalancingNotifySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbLoadBalancingNotifySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44e44c05-6bdf-4f02-acdb-b03a136d9a3a">OnGetMostSuitableTarget</a>
</td>
<td align="left" width="63%">
Returns a load-balancing result to RD Connection Broker.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/11ef1bd4-301f-456b-a68b-2f32b75ac5ae">ITsSbBaseNotifySink</a>



<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

