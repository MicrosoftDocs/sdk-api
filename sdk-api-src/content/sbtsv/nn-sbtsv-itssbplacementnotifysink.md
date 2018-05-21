---
UID: NN:sbtsv.ITsSbPlacementNotifySink
title: ITsSbPlacementNotifySink
author: windows-driver-content
description: Exposes methods that return information about environments to Remote Desktop Connection Broker (RD Connection Broker).
old-location: termserv\itssbplacementnotifysink.htm
old-project: TermServ
ms.assetid: 7abc5454-141a-47bc-b9cd-341b41a093d2
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: ITsSbPlacementNotifySink, ITsSbPlacementNotifySink interface [Remote Desktop Services], ITsSbPlacementNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbPlacementNotifySink, termserv.itssbplacementnotifysink
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
req.typenames: TS_SB_SORT_BY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sbtsv.h
api_name:
-	ITsSbPlacementNotifySink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITsSbPlacementNotifySink interface


## -description


Exposes methods that return information about environments to 
   Remote Desktop Connection Broker (RD Connection Broker).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbPlacementNotifySink</b> interface inherits from <a href="https://msdn.microsoft.com/11ef1bd4-301f-456b-a68b-2f32b75ac5ae">ITsSbBaseNotifySink</a>. <b>ITsSbPlacementNotifySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbPlacementNotifySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/937982aa-7655-4681-ba6c-94201743c90c">OnQueryEnvironmentCompleted</a>
</td>
<td align="left" width="63%">
Notifies RD Connection Broker that the environment specified by the 
       <a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a> object is already 
       hosting the correct target.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/11ef1bd4-301f-456b-a68b-2f32b75ac5ae">ITsSbBaseNotifySink</a>



<a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a>



<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

