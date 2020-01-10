---
UID: NN:tapi3cc.IEnumAgent
title: IEnumAgent (tapi3cc.h)
description: Enumerator interface for ITAgent.
old-location: tapi3\ienumagent.htm
tech.root: Tapi
ms.assetid: 4c75314c-72f0-4eae-a1f5-36f3959c322a
ms.date: 12/05/2018
ms.keywords: IEnumAgent, IEnumAgent interface [TAPI 2.2], IEnumAgent interface [TAPI 2.2],described, _tapi3_ienumagent, tapi3.ienumagent, tapi3cc/IEnumAgent
f1_keywords:
- tapi3cc/IEnumAgent
dev_langs:
- c++
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
- IEnumAgent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumAgent interface


## -description


Enumerator interface for 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumAgent</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumAgent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumAgent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumagent-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumagent-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumagent-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumagent-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>
 

 

