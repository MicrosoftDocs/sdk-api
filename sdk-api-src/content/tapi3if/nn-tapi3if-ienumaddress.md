---
UID: NN:tapi3if.IEnumAddress
title: IEnumAddress (tapi3if.h)
description: The IEnumAddress interface provides COM-standard enumeration methods for the ITAddress interface. The ITTAPI::EnumerateAddresses and ITAgentHandler::EnumerateUsableAddresses methods return a pointer to IEnumAddress.helpviewer_keywords: ["IEnumAddress","IEnumAddress interface [TAPI 2.2]","IEnumAddress interface [TAPI 2.2]","described","_tapi3_ienumaddress","tapi3.ienumaddress","tapi3if/IEnumAddress"]
old-location: tapi3\ienumaddress.htm
tech.root: Tapi
ms.assetid: bfe9f12e-ceb7-4120-8193-70feb2bc7c85
ms.date: 12/05/2018
ms.keywords: IEnumAddress, IEnumAddress interface [TAPI 2.2], IEnumAddress interface [TAPI 2.2],described, _tapi3_ienumaddress, tapi3.ienumaddress, tapi3if/IEnumAddress
f1_keywords:
- tapi3if/IEnumAddress
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- IEnumAddress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumAddress interface


## -description


The 
<b>IEnumAddress</b> interface provides COM-standard enumeration methods for the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses">ITTAPI::EnumerateAddresses</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-enumerateusableaddresses">ITAgentHandler::EnumerateUsableAddresses</a> methods return a pointer to 
<b>IEnumAddress</b>.

The 
<b>IEnumAddress</b> interface is hidden from Visual Basic and scripting languages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumAddress</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumAddress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumAddress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumaddress-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumaddress-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumaddress-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumaddress-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>
 

 

