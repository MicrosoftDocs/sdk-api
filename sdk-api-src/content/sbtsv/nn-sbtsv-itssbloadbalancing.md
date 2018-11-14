---
UID: NN:sbtsv.ITsSbLoadBalancing
title: ITsSbLoadBalancing
author: windows-sdk-content
description: Exposes methods you can use to provide a custom load-balancing algorithm.
old-location: termserv\itssbloadbalancing.htm
tech.root: termserv
ms.assetid: 2dc9dd37-0dc1-4b73-bcac-9fb3d1158b54
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITsSbLoadBalancing, ITsSbLoadBalancing interface [Remote Desktop Services], ITsSbLoadBalancing interface [Remote Desktop Services],described, sbtsv/ITsSbLoadBalancing, termserv.itssbloadbalancing
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
 - ITsSbLoadBalancing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbLoadBalancing interface


## -description


Exposes methods you can use to provide a custom load-balancing algorithm.

The 
<a href="https://msdn.microsoft.com/4f625f64-3909-4003-938c-7807ec24e59e">GetMostSuitableTarget</a> method should return an endpoint (target) to which the client 
connects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbLoadBalancing</b> interface inherits from <a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a>. <b>ITsSbLoadBalancing</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbLoadBalancing</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f625f64-3909-4003-938c-7807ec24e59e">GetMostSuitableTarget</a>
</td>
<td align="left" width="63%">
Determines the most suitable target to which to direct an incoming client 
connection.

</td>
</tr>
</table> 


## -remarks



A plug-in can implement this interface to provide a custom load-balancing algorithm.




## -see-also




<a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a>



<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

