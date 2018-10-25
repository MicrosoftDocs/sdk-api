---
UID: NF:sbtsv.ITsSbLoadBalancing.GetMostSuitableTarget
title: ITsSbLoadBalancing::GetMostSuitableTarget
author: windows-sdk-content
description: Determines the most suitable target to which to direct an incoming client connection.
old-location: termserv\itssbloadbalancing_getmostsuitabletarget.htm
tech.root: termserv
ms.assetid: 4f625f64-3909-4003-938c-7807ec24e59e
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: GetMostSuitableTarget, GetMostSuitableTarget method [Remote Desktop Services], GetMostSuitableTarget method [Remote Desktop Services],ITsSbLoadBalancing interface, ITsSbLoadBalancing interface [Remote Desktop Services],GetMostSuitableTarget method, ITsSbLoadBalancing.GetMostSuitableTarget, ITsSbLoadBalancing::GetMostSuitableTarget, sbtsv/ITsSbLoadBalancing::GetMostSuitableTarget, termserv.itssbloadbalancing_getmostsuitabletarget
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbLoadBalancing::GetMostSuitableTarget


## -description


Determines the most suitable target to which to direct an incoming client 
connection.

Remote Desktop Connection Broker (RD Connection Broker) calls this method when it needs to redirect an incoming client connection.


## -parameters




### -param pConnection [in]

A pointer to an <a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a> object. Information specific to a client connection, such as user name and 
farm name, can be obtained from this object.


### -param pLBSink [in]

A pointer to an <a href="https://msdn.microsoft.com/cc6d2616-27e1-4731-91bf-fe96bcea2cab">ITsSbLoadBalancingNotifySink</a> object. If the plug-in successfully determines where to redirect the connection, it should return the load balancing result by using this sink object. For more information, see <a href="https://msdn.microsoft.com/f19f006c-e74a-4f44-8be8-f71852d4c305">ITsSbLoadBalanceResult</a>.


## -returns



This method can return one of these values.


If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list.






## -remarks



The default load-balancing algorithm in RD Connection Broker redirects an incoming connection to the server with the 
fewest remote sessions. Your plug-in can use this method to override the default load-balancing algorithm. For example, you could define an algorithm that assigns connections to servers by comparing resource use on the target servers. You could also redirect the connection based on the 
 information in the client connection object, such as the <a href="https://msdn.microsoft.com/8734b130-f1fd-4107-b0cc-482b78647ac7">InitialProgram</a> property.




## -see-also




<a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a>



<a href="https://msdn.microsoft.com/f19f006c-e74a-4f44-8be8-f71852d4c305">ITsSbLoadBalanceResult</a>



<a href="https://msdn.microsoft.com/2dc9dd37-0dc1-4b73-bcac-9fb3d1158b54">ITsSbLoadBalancing</a>



<a href="https://msdn.microsoft.com/cc6d2616-27e1-4731-91bf-fe96bcea2cab">ITsSbLoadBalancingNotifySink</a>
 

 

