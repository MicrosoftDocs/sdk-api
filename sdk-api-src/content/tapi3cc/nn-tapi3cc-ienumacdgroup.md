---
UID: NN:tapi3cc.IEnumACDGroup
title: IEnumACDGroup
author: windows-sdk-content
description: The IEnumACDGroup interface provides COM-standard enumeration methods for the ITACDGroup interface. The ITAgentHandler::EnumerateACDGroups method returns a pointer to IEnumACDGroup.
old-location: tapi3\ienumacdgroup.htm
tech.root: TAPI
ms.assetid: 301cd27e-00ac-44a4-b5c6-0efcb36ad974
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IEnumACDGroup, IEnumACDGroup interface [TAPI 2.2], IEnumACDGroup interface [TAPI 2.2],described, _tapi3_ienumacdgroup, tapi3.ienumacdgroup, tapi3cc/IEnumACDGroup
ms.prod: windows
ms.technology: windows-sdk
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
 - IEnumACDGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/202f8534-9990-4e69-b3b8-8a8884b651f1">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20cad3aa-2c8c-4ef8-bb3a-b7662b125475">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66c51bdd-c820-4670-a80d-27cfa080f08f">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58f794cc-da10-4772-9afe-078337b7734b">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a>
 

 

