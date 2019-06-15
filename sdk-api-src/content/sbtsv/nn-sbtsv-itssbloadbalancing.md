---
UID: NN:sbtsv.ITsSbLoadBalancing
title: ITsSbLoadBalancing (sbtsv.h)
author: windows-sdk-content
description: Exposes methods you can use to provide a custom load-balancing algorithm.
old-location: termserv\itssbloadbalancing.htm
tech.root: TermServ
ms.assetid: 2dc9dd37-0dc1-4b73-bcac-9fb3d1158b54
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITsSbLoadBalancing, ITsSbLoadBalancing interface [Remote Desktop Services], ITsSbLoadBalancing interface [Remote Desktop Services],described, sbtsv/ITsSbLoadBalancing, termserv.itssbloadbalancing
ms.topic: interface
f1_keywords: ["sbtsv/ITsSbLoadBalancing"]
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
ms.custom: 19H1
---

# ITsSbLoadBalancing interface


## -description


Exposes methods you can use to provide a custom load-balancing algorithm.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbloadbalancing-getmostsuitabletarget">GetMostSuitableTarget</a> method should return an endpoint (target) to which the client 
connects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbLoadBalancing</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>. <b>ITsSbLoadBalancing</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbloadbalancing-getmostsuitabletarget">GetMostSuitableTarget</a>
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




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
 

 

