---
UID: NF:tapi3if.IEnumCallingCard.Reset
title: IEnumCallingCard::Reset (tapi3if.h)
description: The Reset method resets to the beginning of the enumeration sequence. This method is hidden from Visual Basic and scripting languages. (IEnumCallingCard.Reset)
helpviewer_keywords: ["IEnumCallingCard interface [TAPI 2.2]","Reset method","IEnumCallingCard.Reset","IEnumCallingCard::Reset","Reset","Reset method [TAPI 2.2]","Reset method [TAPI 2.2]","IEnumCallingCard interface","_tapi3_ienumcallingcard_reset","tapi3.ienumcallingcard_reset","tapi3if/IEnumCallingCard::Reset"]
old-location: tapi3\ienumcallingcard_reset.htm
tech.root: tapi3
ms.assetid: 406e4f37-86b6-46bf-97b9-e9944f56bc0d
ms.date: 12/05/2018
ms.keywords: IEnumCallingCard interface [TAPI 2.2],Reset method, IEnumCallingCard.Reset, IEnumCallingCard::Reset, Reset, Reset method [TAPI 2.2], Reset method [TAPI 2.2],IEnumCallingCard interface, _tapi3_ienumcallingcard_reset, tapi3.ienumcallingcard_reset, tapi3if/IEnumCallingCard::Reset
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
 - IEnumCallingCard::Reset
 - tapi3if/IEnumCallingCard::Reset
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
 - IEnumCallingCard.Reset
---

# IEnumCallingCard::Reset


## -description

The 
<b>Reset</b> method resets to the beginning of the enumeration sequence. This method is hidden from Visual Basic and scripting languages.



## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>
