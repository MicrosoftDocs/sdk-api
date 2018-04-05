---
UID: NN:sbtsv.ITsSbOrchestrationNotifySink
title: ITsSbOrchestrationNotifySink
author: windows-driver-content
description: Exposes methods that return an ITsSbTarget object to Remote Desktop Connection Broker (RD Connection Broker) after the target is successfully prepared for a connection.
old-location: termserv\itssborchestrationnotifysink.htm
old-project: TermServ
ms.assetid: 767b6e73-ee0d-4802-99ff-ac37880a0884
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ITsSbOrchestrationNotifySink, ITsSbOrchestrationNotifySink interface [Remote Desktop Services], ITsSbOrchestrationNotifySink interface [Remote Desktop Services], described, sbtsv/ITsSbOrchestrationNotifySink, termserv.itssborchestrationnotifysink
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
-	ITsSbOrchestrationNotifySink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ITsSbOrchestrationNotifySink interface


## -description


Exposes methods that return an <a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a> object to Remote Desktop Connection Broker (RD Connection Broker) after the target is successfully prepared for a connection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbOrchestrationNotifySink</b> interface inherits from <a href="https://msdn.microsoft.com/11ef1bd4-301f-456b-a68b-2f32b75ac5ae">ITsSbBaseNotifySink</a>. <b>ITsSbOrchestrationNotifySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbOrchestrationNotifySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/781cb67c-75bb-4d3c-8b86-fddbe9511255">OnReadyToConnect</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a> object to RD Connection Broker after the target is successfully prepared for a connection.

</td>
</tr>
</table> 


## -remarks



Plug-ins should use this interface to return an <a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a> object to RD Connection Broker after the plug-in has successfully prepared ("orchestrated") the target.




## -see-also




<a href="https://msdn.microsoft.com/11ef1bd4-301f-456b-a68b-2f32b75ac5ae">ITsSbBaseNotifySink</a>



<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

