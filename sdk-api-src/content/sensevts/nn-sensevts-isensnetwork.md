---
UID: NN:sensevts.ISensNetwork
title: ISensNetwork
author: windows-driver-content
description: The ISensNetwork interface handles network events fired by the System Event Notification Service (SENS).
old-location: sens\isensnetwork.htm
old-project: Sens
ms.assetid: 1cea5dff-13ea-4afb-84ac-7b8df4f55fc8
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ISensNetwork, ISensNetwork interface [SENS], ISensNetwork interface [SENS], described, _zaw_isensnetwork, sens.isensnetwork, sensevts/ISensNetwork, syncmgr.isensnetwork
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: sensevts.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Sensevts.tlb
req.typenames: QOCINFO, *LPQOCINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Sens.dll
api_name:
-	ISensNetwork
product: Windows
targetos: Windows
req.lib: 
req.dll: Sens.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ISensNetwork interface


## -description


The 
<b>ISensNetwork</b> interface handles network events fired by the System Event Notification Service (SENS).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISensNetwork</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ISensNetwork</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISensNetwork</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b91e46b9-7931-4959-97de-fa882a56e406">ConnectionLost</a>
</td>
<td align="left" width="63%">
Specified connection has been dropped.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b067a6f-ba4c-4914-aa5b-e0fd7690e75c">ConnectionMade</a>
</td>
<td align="left" width="63%">
Specified connection has been established.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a27dd3c7-e3f6-4ccb-b23a-17b15235245c">ConnectionMadeNoQOCInfo</a>
</td>
<td align="left" width="63%">
Specified connection has been established with no Quality of Connection information available.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="https://msdn.microsoft.com/77c02510-6386-4f6d-af1a-e7337f5d347d">ISensLogon</a>



<a href="https://msdn.microsoft.com/39d483be-8dbd-41f9-9804-af9dc4535c05">ISensOnNow</a>
 

 

