---
UID: NN:tapi3.IEnumAgentSession
title: IEnumAgentSession
author: windows-sdk-content
description: The IEnumAgentSession interface provides COM-standard enumeration methods for the ITAgentSession interface. The ITAgent::EnumerateAgentSessions method returns a pointer to IEnumAgentSession.
old-location: tapi3\ienumagentsession.htm
old-project: Tapi
ms.assetid: 38b9fc57-a0af-4dfa-9058-e721138c8be9
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IEnumAgentSession, IEnumAgentSession interface [TAPI 2.2], IEnumAgentSession interface [TAPI 2.2],described, _tapi3_ienumagentsession, tapi3.ienumagentsession, tapi3cc/IEnumAgentSession
ms.prod: windows
ms.technology: windows-sdk
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
-	IEnumAgentSession
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumAgentSession interface


## -description


The 
<b>IEnumAgentSession</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a> interface. The 
<a href="https://msdn.microsoft.com/6b639a41-c866-49ad-bc33-1215da7c8a19">ITAgent::EnumerateAgentSessions</a> method returns a pointer to 
<b>IEnumAgentSession</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumAgentSession</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumAgentSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumAgentSession</b> interface has these methods.
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

