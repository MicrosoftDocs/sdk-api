---
UID: NN:tapi3if.IEnumBstr
title: IEnumBstr (tapi3if.h)
description: The IEnumBstr interface provides COM-standard methods to enumerate BSTR strings.
helpviewer_keywords: ["IEnumBstr","IEnumBstr interface [TAPI 2.2]","IEnumBstr interface [TAPI 2.2]","described","_tapi3_ienumbstr","tapi3.ienumbstr","tapi3if/IEnumBstr"]
old-location: tapi3\ienumbstr.htm
tech.root: tapi3
ms.assetid: 0e87ec06-7f3a-410c-9d54-7a67991e089c
ms.date: 12/05/2018
ms.keywords: IEnumBstr, IEnumBstr interface [TAPI 2.2], IEnumBstr interface [TAPI 2.2],described, _tapi3_ienumbstr, tapi3.ienumbstr, tapi3if/IEnumBstr
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
 - IEnumBstr
 - tapi3if/IEnumBstr
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
 - IEnumBstr
---

# IEnumBstr interface


## -description

The 
<b>IEnumBstr</b> interface provides COM-standard methods to enumerate <b>BSTR</b> strings. The following methods return a pointer to this interface:
<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-enumeratecalltreatments">ITAddressCapabilities::EnumerateCallTreatments</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-enumeratecompletionmessages">ITAddressCapabilities::EnumerateCompletionMessages</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-enumeratedeviceclasses">ITAddressCapabilities::EnumerateDeviceClasses</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses">IMcastLeaseInfo::EnumerateAddresses</a>
</li>
</ul>The 
<b>IEnumBstr</b> interface is hidden from Visual Basic and scripting languages.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumBstr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumBstr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumBstr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumbstr-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumbstr-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumbstr-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumbstr-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table>

