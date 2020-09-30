---
UID: NN:comcat.IEnumCATEGORYINFO
title: IEnumCATEGORYINFO (comcat.h)
description: Enumerates component categories registered in the system.
helpviewer_keywords: ["IEnumCATEGORYINFO","IEnumCATEGORYINFO interface [COM]","IEnumCATEGORYINFO interface [COM]","described","_com_ienumcategoryinfo","com.ienumcategoryinfo","comcat/IEnumCATEGORYINFO"]
old-location: com\ienumcategoryinfo.htm
tech.root: com
ms.assetid: 87469ace-ae34-40e5-aab6-f26a4bc50b54
ms.date: 12/05/2018
ms.keywords: IEnumCATEGORYINFO, IEnumCATEGORYINFO interface [COM], IEnumCATEGORYINFO interface [COM],described, _com_ienumcategoryinfo, com.ienumcategoryinfo, comcat/IEnumCATEGORYINFO
req.header: comcat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Comcat.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumCATEGORYINFO
 - comcat/IEnumCATEGORYINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComCat.h
api_name:
 - IEnumCATEGORYINFO
---

# IEnumCATEGORYINFO interface


## -description

Enumerates component categories registered in the system.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumCATEGORYINFO</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumCATEGORYINFO</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumCATEGORYINFO</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comcat/nf-comcat-ienumcategoryinfo-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comcat/nf-comcat-ienumcategoryinfo-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comcat/nf-comcat-ienumcategoryinfo-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comcat/nf-comcat-ienumcategoryinfo-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table>