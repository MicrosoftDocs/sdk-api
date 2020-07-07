---
UID: NN:comcat.IEnumGUID
title: IEnumGUID (comcat.h)
description: Enables clients to enumerate through a collection of class IDs for COM classes.
helpviewer_keywords: ["IEnumGUID","IEnumGUID interface [COM]","IEnumGUID interface [COM]","described","_com_ienumguid","com.ienumguid","comcat/IEnumGUID"]
old-location: com\ienumguid.htm
tech.root: com
ms.assetid: 4f2e0f96-a471-4883-be41-d93806461020
ms.date: 12/05/2018
ms.keywords: IEnumGUID, IEnumGUID interface [COM], IEnumGUID interface [COM],described, _com_ienumguid, com.ienumguid, comcat/IEnumGUID
f1_keywords:
- comcat/IEnumGUID
dev_langs:
- c++
req.header: comcat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComCat.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComCat.h
api_name:
- IEnumGUID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumGUID interface


## -description


Enables clients to enumerate through a collection of class IDs for COM classes.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumGUID</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumGUID</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumGUID</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-ienumguid-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-ienumguid-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-ienumguid-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-ienumguid-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


## -remarks



Alternate names for this interface are <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd542667(v=vs.85)">IEnumCLSID</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd542661(v=vs.85)">IEnumCATID</a>.



