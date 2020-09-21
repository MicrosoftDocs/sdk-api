---
UID: NN:tapi3if.IEnumCallingCard
title: IEnumCallingCard (tapi3if.h)
description: The IEnumCallingCard interface provides COM-standard enumeration methods for the ITCallingCard interface. The ITAddressTranslation::EnumerateCallingCards method returns a pointer to IEnumCallingCard.
helpviewer_keywords: ["IEnumCallingCard","IEnumCallingCard interface [TAPI 2.2]","IEnumCallingCard interface [TAPI 2.2]","described","_tapi3_ienumcallingcard","tapi3.ienumcallingcard","tapi3if/IEnumCallingCard"]
old-location: tapi3\ienumcallingcard.htm
tech.root: tapi3
ms.assetid: d2eed88b-9a01-4205-a35d-92a24e07a1e2
ms.date: 12/05/2018
ms.keywords: IEnumCallingCard, IEnumCallingCard interface [TAPI 2.2], IEnumCallingCard interface [TAPI 2.2],described, _tapi3_ienumcallingcard, tapi3.ienumcallingcard, tapi3if/IEnumCallingCard
req.header: tapi3if.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumCallingCard
 - tapi3if/IEnumCallingCard
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumCallingCard
---

# IEnumCallingCard interface


## -description

The 
<b>IEnumCallingCard</b> interface provides COM-standard enumeration methods for the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard">ITCallingCard</a> interface. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-enumeratecallingcards">ITAddressTranslation::EnumerateCallingCards</a> method returns a pointer to 
<b>IEnumCallingCard</b>.

The 
<b>IEnumCallingCard</b> interface is hidden from Visual Basic and scripting languages.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumCallingCard</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumCallingCard</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumCallingCard</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ienumcallingcard-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ienumcallingcard-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ienumcallingcard-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ienumcallingcard-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>