---
UID: NF:sbtsv.ITsSbLoadBalancing.GetMostSuitableTarget
title: ITsSbLoadBalancing::GetMostSuitableTarget (sbtsv.h)
description: Determines the most suitable target to which to direct an incoming client connection.
helpviewer_keywords: ["GetMostSuitableTarget","GetMostSuitableTarget method [Remote Desktop Services]","GetMostSuitableTarget method [Remote Desktop Services]","ITsSbLoadBalancing interface","ITsSbLoadBalancing interface [Remote Desktop Services]","GetMostSuitableTarget method","ITsSbLoadBalancing.GetMostSuitableTarget","ITsSbLoadBalancing::GetMostSuitableTarget","sbtsv/ITsSbLoadBalancing::GetMostSuitableTarget","termserv.itssbloadbalancing_getmostsuitabletarget"]
old-location: termserv\itssbloadbalancing_getmostsuitabletarget.htm
tech.root: TermServ
ms.assetid: 4f625f64-3909-4003-938c-7807ec24e59e
ms.date: 11/24/2023
ms.keywords: GetMostSuitableTarget, GetMostSuitableTarget method [Remote Desktop Services], GetMostSuitableTarget method [Remote Desktop Services],ITsSbLoadBalancing interface, ITsSbLoadBalancing interface [Remote Desktop Services],GetMostSuitableTarget method, ITsSbLoadBalancing.GetMostSuitableTarget, ITsSbLoadBalancing::GetMostSuitableTarget, sbtsv/ITsSbLoadBalancing::GetMostSuitableTarget, termserv.itssbloadbalancing_getmostsuitabletarget
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
 - ITsSbLoadBalancing::GetMostSuitableTarget
 - sbtsv/ITsSbLoadBalancing::GetMostSuitableTarget
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
 - ITsSbLoadBalancing.GetMostSuitableTarget
---

## -description

This is a callback method that you implement in your app, in order to determines the most suitable target to which to direct an incoming client connection. The Remote Desktop Connection Broker (RD Connection Broker) calls your implementation when the broker needs to redirect an incoming client connection. 

## -parameters

### -param pConnection [in]

A pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a> object. Information specific to a client connection, such as user name and 
farm name, can be obtained from this object.

### -param pLBSink [in]

A pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink">ITsSbLoadBalancingNotifySink</a> object. If the plug-in successfully determines where to redirect the connection, it should return the load balancing result by using this sink object. For more information, see <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult">ITsSbLoadBalanceResult</a>.

## -returns

If the method succeeds, then return **S_OK**. Otherwise, indicate failure by returning *any* failure **HRESULT**. But if you want your plug-in to indicate that it has failed to determine a target, then you can return **E_SB_LOAD_BAL_FAILED**.

## -remarks

The default load-balancing algorithm in RD Connection Broker redirects an incoming connection to the server with the 
fewest remote sessions. Your plug-in can use this method to override the default load-balancing algorithm. For example, you could define an algorithm that assigns connections to servers by comparing resource use on the target servers. You could also redirect the connection based on the 
 information in the client connection object, such as the <a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbclientconnection-get_initialprogram">InitialProgram</a> property.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult">ITsSbLoadBalanceResult</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing">ITsSbLoadBalancing</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink">ITsSbLoadBalancingNotifySink</a>
