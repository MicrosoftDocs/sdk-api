---
UID: NF:sbtsv.ITsSbLoadBalancing.GetMostSuitableTarget
title: ITsSbLoadBalancing::GetMostSuitableTarget (sbtsv.h)
description: Determines the most suitable target to which to direct an incoming client connection.
helpviewer_keywords: ["GetMostSuitableTarget","GetMostSuitableTarget method [Remote Desktop Services]","GetMostSuitableTarget method [Remote Desktop Services]","ITsSbLoadBalancing interface","ITsSbLoadBalancing interface [Remote Desktop Services]","GetMostSuitableTarget method","ITsSbLoadBalancing.GetMostSuitableTarget","ITsSbLoadBalancing::GetMostSuitableTarget","sbtsv/ITsSbLoadBalancing::GetMostSuitableTarget","termserv.itssbloadbalancing_getmostsuitabletarget"]
old-location: termserv\itssbloadbalancing_getmostsuitabletarget.htm
tech.root: TermServ
ms.assetid: 4f625f64-3909-4003-938c-7807ec24e59e
ms.date: 12/05/2018
ms.keywords: GetMostSuitableTarget, GetMostSuitableTarget method [Remote Desktop Services], GetMostSuitableTarget method [Remote Desktop Services],ITsSbLoadBalancing interface, ITsSbLoadBalancing interface [Remote Desktop Services],GetMostSuitableTarget method, ITsSbLoadBalancing.GetMostSuitableTarget, ITsSbLoadBalancing::GetMostSuitableTarget, sbtsv/ITsSbLoadBalancing::GetMostSuitableTarget, termserv.itssbloadbalancing_getmostsuitabletarget
f1_keywords:
- sbtsv/ITsSbLoadBalancing.GetMostSuitableTarget
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
- ITsSbLoadBalancing.GetMostSuitableTarget
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbLoadBalancing::GetMostSuitableTarget


## -description


Determines the most suitable target to which to direct an incoming client 
connection.

Remote Desktop Connection Broker (RD Connection Broker) calls this method when it needs to redirect an incoming client connection.


## -parameters




### -param pConnection [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a> object. Information specific to a client connection, such as user name and 
farm name, can be obtained from this object.


### -param pLBSink [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink">ITsSbLoadBalancingNotifySink</a> object. If the plug-in successfully determines where to redirect the connection, it should return the load balancing result by using this sink object. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult">ITsSbLoadBalanceResult</a>.


## -returns



This method can return one of these values.


If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list.






## -remarks



The default load-balancing algorithm in RD Connection Broker redirects an incoming connection to the server with the 
fewest remote sessions. Your plug-in can use this method to override the default load-balancing algorithm. For example, you could define an algorithm that assigns connections to servers by comparing resource use on the target servers. You could also redirect the connection based on the 
 information in the client connection object, such as the <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbclientconnection-get_initialprogram">InitialProgram</a> property.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult">ITsSbLoadBalanceResult</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing">ITsSbLoadBalancing</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink">ITsSbLoadBalancingNotifySink</a>
 

 

