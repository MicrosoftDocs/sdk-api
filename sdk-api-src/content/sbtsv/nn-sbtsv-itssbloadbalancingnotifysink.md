---
UID: NN:sbtsv.ITsSbLoadBalancingNotifySink
title: ITsSbLoadBalancingNotifySink (sbtsv.h)
description: Exposes methods that return the result of a load-balancing algorithm to Remote Desktop Connection Broker (RD Connection Broker).helpviewer_keywords: ["ITsSbLoadBalancingNotifySink","ITsSbLoadBalancingNotifySink interface [Remote Desktop Services]","ITsSbLoadBalancingNotifySink interface [Remote Desktop Services]","described","sbtsv/ITsSbLoadBalancingNotifySink","termserv.itssbloadbalancingnotifysink"]
old-location: termserv\itssbloadbalancingnotifysink.htm
tech.root: TermServ
ms.assetid: cc6d2616-27e1-4731-91bf-fe96bcea2cab
ms.date: 12/05/2018
ms.keywords: ITsSbLoadBalancingNotifySink, ITsSbLoadBalancingNotifySink interface [Remote Desktop Services], ITsSbLoadBalancingNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbLoadBalancingNotifySink, termserv.itssbloadbalancingnotifysink
f1_keywords:
- sbtsv/ITsSbLoadBalancingNotifySink
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbLoadBalancingNotifySink interface


## -description


Exposes methods that return the result of a load-balancing algorithm to Remote Desktop Connection Broker (RD Connection Broker).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbLoadBalancingNotifySink</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink">ITsSbBaseNotifySink</a>. <b>ITsSbLoadBalancingNotifySink</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbloadbalancingnotifysink-ongetmostsuitabletarget">OnGetMostSuitableTarget</a>
</td>
<td align="left" width="63%">
Returns a load-balancing result to RD Connection Broker.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink">ITsSbBaseNotifySink</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
 

 

