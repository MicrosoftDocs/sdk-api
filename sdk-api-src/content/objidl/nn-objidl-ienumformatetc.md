---
UID: NN:objidl.IEnumFORMATETC
title: IEnumFORMATETC (objidl.h)
description: Enumerates the FORMATETC structures that define the formats and media supported by a given data object.
helpviewer_keywords: ["IEnumFORMATETC","IEnumFORMATETC interface [COM]","IEnumFORMATETC interface [COM]","described","_ole_ienumformatetc","com.ienumformatetc","objidl/IEnumFORMATETC"]
old-location: com\ienumformatetc.htm
tech.root: com
ms.assetid: 4d180fdd-2d58-4d26-9242-6552dda0d3e6
ms.date: 12/05/2018
ms.keywords: IEnumFORMATETC, IEnumFORMATETC interface [COM], IEnumFORMATETC interface [COM],described, _ole_ienumformatetc, com.ienumformatetc, objidl/IEnumFORMATETC
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IEnumFORMATETC
 - objidl/IEnumFORMATETC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IEnumFORMATETC
---

# IEnumFORMATETC interface


## -description

Enumerates the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structures that define the formats and media supported by a given data object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumFORMATETC</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumFORMATETC</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumFORMATETC</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/objidl/nf-objidl-ienumformatetc-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/objidl/nf-objidl-ienumformatetc-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/objidl/nf-objidl-ienumformatetc-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/objidl/nf-objidl-ienumformatetc-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table>