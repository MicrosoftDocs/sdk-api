---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

