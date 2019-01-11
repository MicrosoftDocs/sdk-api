---
UID: NN:sbtsv.ITsSbOrchestration
title: ITsSbOrchestration
author: windows-sdk-content
description: Exposes methods that Remote Desktop Connection Broker (RD Connection Broker) uses to ensure that the target is ready before a client is redirected to it.
old-location: termserv\itssborchestration.htm
tech.root: TermServ
ms.assetid: fae858ae-19e5-453d-b9ef-1da7ea706e49
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITsSbOrchestration, ITsSbOrchestration interface [Remote Desktop Services], ITsSbOrchestration interface [Remote Desktop Services],described, sbtsv/ITsSbOrchestration, termserv.itssborchestration
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
 - ITsSbOrchestration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbOrchestration interface


## -description


Exposes methods that Remote Desktop Connection Broker (RD Connection Broker) uses to ensure that the target is ready before a client is redirected to it.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbOrchestration</b> interface inherits from <a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a>. <b>ITsSbOrchestration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbOrchestration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46ffad8a-bafc-426f-9963-9a6f6f60329b">PrepareTargetForConnect</a>
</td>
<td align="left" width="63%">
Prepares the target for a client connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a>



<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

