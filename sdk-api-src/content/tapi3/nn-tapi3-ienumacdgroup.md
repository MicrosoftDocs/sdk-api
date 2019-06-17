---
UID: NN:tapi3.IEnumACDGroup
title: IEnumACDGroup (tapi3.h)
author: windows-sdk-content
description: The IEnumACDGroup interface provides COM-standard enumeration methods for the ITACDGroup interface. The ITAgentHandler::EnumerateACDGroups method returns a pointer to IEnumACDGroup.
old-location: tapi3\ienumacdgroup.htm
tech.root: Tapi
ms.assetid: 301cd27e-00ac-44a4-b5c6-0efcb36ad974
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumACDGroup, IEnumACDGroup interface [TAPI 2.2], IEnumACDGroup interface [TAPI 2.2],described, _tapi3_ienumacdgroup, tapi3.ienumacdgroup, tapi3cc/IEnumACDGroup
ms.topic: interface
f1_keywords: ["tapi3/IEnumACDGroup"]
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
 - IEnumACDGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumACDGroup interface


## -description


The 
<b>IEnumACDGroup</b> interface provides COM-standard enumeration methods for the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a> interface. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-enumerateacdgroups">ITAgentHandler::EnumerateACDGroups</a> method returns a pointer to 
<b>IEnumACDGroup</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumACDGroup</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumACDGroup</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumacdgroup-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumacdgroup-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumacdgroup-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumacdgroup-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a>
 

 

