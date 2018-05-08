---
UID: NN:sbtsv.ITsSbBaseNotifySink
title: ITsSbBaseNotifySink
author: windows-driver-content
description: Exposes methods that report status and error messages to Remote Desktop Connection Broker (RD Connection Broker).
old-location: termserv\itssbbasenotifysink.htm
old-project: TermServ
ms.assetid: 11ef1bd4-301f-456b-a68b-2f32b75ac5ae
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ITsSbBaseNotifySink, ITsSbBaseNotifySink interface [Remote Desktop Services], ITsSbBaseNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbBaseNotifySink, termserv.itssbbasenotifysink
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
-	ITsSbBaseNotifySink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITsSbBaseNotifySink interface


## -description


Exposes methods that report status and error messages to Remote Desktop Connection Broker (RD Connection Broker).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbBaseNotifySink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITsSbBaseNotifySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbBaseNotifySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8101644-51b4-45a8-8696-7dbb28aaaf0b">OnError</a>
</td>
<td align="left" width="63%">
Reports an error condition to RD Connection Broker. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bde8375-b03a-44b8-9ba5-bc15277f3a4a">OnReportStatus</a>
</td>
<td align="left" width="63%">
Sends status messages to the Remote Desktop Connection (RDC) client regarding the processing of a client 
       connection.

</td>
</tr>
</table> 


## -remarks



Plug-ins can use this interface to report status and error messages to RD Connection Broker.

The RD Connection Broker server and the Remote Desktop Session Host (RD Session Host) server (the redirector) must 
    be running Windows Server 2008 R2, and clients must use RDC 7.0.




## -see-also




<a href="https://msdn.microsoft.com/11ef1bd4-301f-456b-a68b-2f32b75ac5ae">ITsSbBaseNotifySink</a>



<a href="https://msdn.microsoft.com/cc6d2616-27e1-4731-91bf-fe96bcea2cab">ITsSbLoadBalancingNotifySink</a>



<a href="https://msdn.microsoft.com/767b6e73-ee0d-4802-99ff-ac37880a0884">ITsSbOrchestrationNotifySink</a>



<a href="https://msdn.microsoft.com/7abc5454-141a-47bc-b9cd-341b41a093d2">ITsSbPlacementNotifySink</a>



<a href="https://msdn.microsoft.com/c52a3253-74cb-4ff9-a4f3-cb9601c02e7d">ITsSbPluginNotifySink</a>



<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

