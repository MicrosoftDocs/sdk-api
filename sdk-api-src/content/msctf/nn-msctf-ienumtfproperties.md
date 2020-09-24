---
UID: NN:msctf.IEnumTfProperties
title: IEnumTfProperties (msctf.h)
description: The IEnumTfProperties interface is implemented by the TSF manager to provide an enumeration of property objects.
helpviewer_keywords: ["IEnumTfProperties","IEnumTfProperties interface [Text Services Framework]","IEnumTfProperties interface [Text Services Framework]","described","_tsf_ienumtfproperties_ref","msctf/IEnumTfProperties","tsf.ienumtfproperties"]
old-location: tsf\ienumtfproperties.htm
tech.root: TSF
ms.assetid: 99d8564f-98bc-4f30-bff9-923a4016a5fe
ms.date: 12/05/2018
ms.keywords: IEnumTfProperties, IEnumTfProperties interface [Text Services Framework], IEnumTfProperties interface [Text Services Framework],described, _tsf_ienumtfproperties_ref, msctf/IEnumTfProperties, tsf.ienumtfproperties
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - IEnumTfProperties
 - msctf/IEnumTfProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - IEnumTfProperties
---

# IEnumTfProperties interface


## -description

The <b>IEnumTfProperties</b> interface is implemented by the TSF manager to provide an enumeration of property objects.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfProperties</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTfProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next">Next</a>
</td>
<td align="left" width="63%">
Obtains the specified number of elements in the enumeration sequence from the current position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-skip">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table>