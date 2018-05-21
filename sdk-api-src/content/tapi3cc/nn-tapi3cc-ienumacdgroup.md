---
UID: NN:tapi3cc.IEnumACDGroup
title: IEnumACDGroup
author: windows-driver-content
description: The IEnumACDGroup interface provides COM-standard enumeration methods for the ITACDGroup interface. The ITAgentHandler::EnumerateACDGroups method returns a pointer to IEnumACDGroup.
old-location: tapi3\ienumacdgroup.htm
old-project: Tapi
ms.assetid: 301cd27e-00ac-44a4-b5c6-0efcb36ad974
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IEnumACDGroup, IEnumACDGroup interface [TAPI 2.2], IEnumACDGroup interface [TAPI 2.2],described, _tapi3_ienumacdgroup, tapi3.ienumacdgroup, tapi3cc/IEnumACDGroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tapi3cc.h
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
req.typenames: AGENT_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	IEnumACDGroup
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumACDGroup interface


## -description


The 
<b>IEnumACDGroup</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a> interface. The 
<a href="https://msdn.microsoft.com/a9078166-ff6a-4520-8209-e785bd6e7100">ITAgentHandler::EnumerateACDGroups</a> method returns a pointer to 
<b>IEnumACDGroup</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumACDGroup</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumACDGroup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumACDGroup</b> interface has these methods.
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


## -see-also




<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a>
 

 

