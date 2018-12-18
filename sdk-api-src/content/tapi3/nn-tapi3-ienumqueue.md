---
UID: NN:tapi3.IEnumQueue
title: IEnumQueue
author: windows-sdk-content
description: The IEnumQueue interface provides COM-standard enumeration methods for the ITQueue interface. The ITACDGroup::EnumerateQueues method returns a pointer to IEnumQueue.
old-location: tapi3\ienumqueue.htm
tech.root: tapi
ms.assetid: 0bbe3533-d5ce-447b-82e1-3bd61c5a7ca2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumQueue, IEnumQueue interface [TAPI 2.2], IEnumQueue interface [TAPI 2.2],described, _tapi3_ienumqueue, tapi3.ienumqueue, tapi3cc/IEnumQueue
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumQueue interface


## -description


The 
<b>IEnumQueue</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023">ITQueue</a> interface. The 
<a href="https://msdn.microsoft.com/1d9e0dcf-ce43-494f-8adc-845d2856bdd1">ITACDGroup::EnumerateQueues</a> method returns a pointer to 
<b>IEnumQueue</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumQueue</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumQueue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumQueue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e63df5aa-8c90-4978-a63f-96ac5f624ef4">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95c1a919-4138-49c1-ad3a-2b15d928e84f">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f444d56-e660-48c3-a483-256138d49984">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92862b33-ceaf-4b18-b782-bb0352871d34">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 

