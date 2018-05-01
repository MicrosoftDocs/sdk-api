---
UID: NF:sbtsv.ITsSbLoadBalancingNotifySink.OnGetMostSuitableTarget
title: ITsSbLoadBalancingNotifySink::OnGetMostSuitableTarget method
author: windows-driver-content
description: Returns a load-balancing result to Remote Desktop Connection Broker (RD Connection Broker).
old-location: termserv\itssbloadbalancingnotifysink_ongetmostsuitabletarget.htm
old-project: TermServ
ms.assetid: 44e44c05-6bdf-4f02-acdb-b03a136d9a3a
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ITsSbLoadBalancingNotifySink, ITsSbLoadBalancingNotifySink interface [Remote Desktop Services], OnGetMostSuitableTarget method, ITsSbLoadBalancingNotifySink::OnGetMostSuitableTarget, OnGetMostSuitableTarget method [Remote Desktop Services], OnGetMostSuitableTarget method [Remote Desktop Services], ITsSbLoadBalancingNotifySink interface, OnGetMostSuitableTarget,ITsSbLoadBalancingNotifySink.OnGetMostSuitableTarget, sbtsv/ITsSbLoadBalancingNotifySink::OnGetMostSuitableTarget, termserv.itssbloadbalancingnotifysink_ongetmostsuitabletarget
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
-	ITsSbLoadBalancingNotifySink.OnGetMostSuitableTarget
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITsSbLoadBalancingNotifySink::OnGetMostSuitableTarget method


## -description


Returns a load-balancing result to Remote Desktop Connection Broker (RD Connection Broker).


## -parameters




### -param pLBResult [in]

A pointer to a <a href="https://msdn.microsoft.com/f19f006c-e74a-4f44-8be8-f71852d4c305">ITsSbLoadBalanceResult</a> object that  includes the name of the target to which the connection should 
be redirected.


### -param fIsNewConnection [in]

Indicates whether this is a new connection. <b>TRUE</b> if it is a new connection; <b>FALSE</b> otherwise.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list.




## -remarks



Your plug-in should call this method on the <a href="https://msdn.microsoft.com/cc6d2616-27e1-4731-91bf-fe96bcea2cab">ITsSbLoadBalancingNotifySink</a> object passed to <a href="https://msdn.microsoft.com/4f625f64-3909-4003-938c-7807ec24e59e">GetMostSuitableTarget</a>.




## -see-also




<a href="https://msdn.microsoft.com/f19f006c-e74a-4f44-8be8-f71852d4c305">ITsSbLoadBalanceResult</a>



<a href="https://msdn.microsoft.com/2dc9dd37-0dc1-4b73-bcac-9fb3d1158b54">ITsSbLoadBalancing</a>



<a href="https://msdn.microsoft.com/cc6d2616-27e1-4731-91bf-fe96bcea2cab">ITsSbLoadBalancingNotifySink</a>
 

 

