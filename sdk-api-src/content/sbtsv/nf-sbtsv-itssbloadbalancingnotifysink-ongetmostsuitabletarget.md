---
UID: NF:sbtsv.ITsSbLoadBalancingNotifySink.OnGetMostSuitableTarget
title: ITsSbLoadBalancingNotifySink::OnGetMostSuitableTarget (sbtsv.h)
description: Returns a load-balancing result to Remote Desktop Connection Broker (RD Connection Broker).
helpviewer_keywords: ["ITsSbLoadBalancingNotifySink interface [Remote Desktop Services]","OnGetMostSuitableTarget method","ITsSbLoadBalancingNotifySink.OnGetMostSuitableTarget","ITsSbLoadBalancingNotifySink::OnGetMostSuitableTarget","OnGetMostSuitableTarget","OnGetMostSuitableTarget method [Remote Desktop Services]","OnGetMostSuitableTarget method [Remote Desktop Services]","ITsSbLoadBalancingNotifySink interface","sbtsv/ITsSbLoadBalancingNotifySink::OnGetMostSuitableTarget","termserv.itssbloadbalancingnotifysink_ongetmostsuitabletarget"]
old-location: termserv\itssbloadbalancingnotifysink_ongetmostsuitabletarget.htm
tech.root: TermServ
ms.assetid: 44e44c05-6bdf-4f02-acdb-b03a136d9a3a
ms.date: 12/05/2018
ms.keywords: ITsSbLoadBalancingNotifySink interface [Remote Desktop Services],OnGetMostSuitableTarget method, ITsSbLoadBalancingNotifySink.OnGetMostSuitableTarget, ITsSbLoadBalancingNotifySink::OnGetMostSuitableTarget, OnGetMostSuitableTarget, OnGetMostSuitableTarget method [Remote Desktop Services], OnGetMostSuitableTarget method [Remote Desktop Services],ITsSbLoadBalancingNotifySink interface, sbtsv/ITsSbLoadBalancingNotifySink::OnGetMostSuitableTarget, termserv.itssbloadbalancingnotifysink_ongetmostsuitabletarget
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbLoadBalancingNotifySink::OnGetMostSuitableTarget
 - sbtsv/ITsSbLoadBalancingNotifySink::OnGetMostSuitableTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbLoadBalancingNotifySink.OnGetMostSuitableTarget
---

# ITsSbLoadBalancingNotifySink::OnGetMostSuitableTarget


## -description

Returns a load-balancing result to Remote Desktop Connection Broker (RD Connection Broker).

## -parameters

### -param pLBResult [in]

A pointer to a <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult">ITsSbLoadBalanceResult</a> object that  includes the name of the target to which the connection should 
be redirected.

### -param fIsNewConnection [in]

Indicates whether this is a new connection. <b>TRUE</b> if it is a new connection; <b>FALSE</b> otherwise.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list.

## -remarks

Your plug-in should call this method on the <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink">ITsSbLoadBalancingNotifySink</a> object passed to <a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbloadbalancing-getmostsuitabletarget">GetMostSuitableTarget</a>.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult">ITsSbLoadBalanceResult</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing">ITsSbLoadBalancing</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink">ITsSbLoadBalancingNotifySink</a>