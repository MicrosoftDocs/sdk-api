---
UID: NN:tapi3.IEnumAgentHandler
title: IEnumAgentHandler
author: windows-driver-content
description: The IEnumAgentHandler interface provides COM-standard enumeration methods for the ITAgentHandler interface. The ITTAPICallCenter::EnumerateAgentHandlers method returns a pointer to IEnumAgentHandler.
old-location: tapi3\ienumagenthandler.htm
old-project: Tapi
ms.assetid: a318318a-769e-4619-a461-4988d90d3f1a
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IEnumAgentHandler, IEnumAgentHandler interface [TAPI 2.2], IEnumAgentHandler interface [TAPI 2.2],described, _tapi3_ienumagenthandler, tapi3.ienumagenthandler, tapi3cc/IEnumAgentHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tapi3.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.typenames: MSP_EVENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	IEnumAgentHandler
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumAgentHandler interface


## -description


The 
<b>IEnumAgentHandler</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a> interface. The 
<a href="https://msdn.microsoft.com/5bd0a926-0d99-4efe-a995-28654c97c97a">ITTAPICallCenter::EnumerateAgentHandlers</a> method returns a pointer to 
<b>IEnumAgentHandler</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumAgentHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumAgentHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumAgentHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 

