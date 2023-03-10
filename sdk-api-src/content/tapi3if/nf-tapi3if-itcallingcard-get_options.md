---
UID: NF:tapi3if.ITCallingCard.get_Options
title: ITCallingCard::get_Options (tapi3if.h)
description: The get_Options method gets the translation options for this address and card.
helpviewer_keywords: ["ITCallingCard interface [TAPI 2.2]","get_Options method","ITCallingCard.get_Options","ITCallingCard::get_Options","_tapi3_itcallingcard_get_options","get_Options","get_Options method [TAPI 2.2]","get_Options method [TAPI 2.2]","ITCallingCard interface","tapi3.itcallingcard_get_options","tapi3if/ITCallingCard::get_Options"]
old-location: tapi3\itcallingcard_get_options.htm
tech.root: tapi3
ms.assetid: 0daa0058-759b-4f4c-8fb4-ce65e4fa9682
ms.date: 12/05/2018
ms.keywords: ITCallingCard interface [TAPI 2.2],get_Options method, ITCallingCard.get_Options, ITCallingCard::get_Options, _tapi3_itcallingcard_get_options, get_Options, get_Options method [TAPI 2.2], get_Options method [TAPI 2.2],ITCallingCard interface, tapi3.itcallingcard_get_options, tapi3if/ITCallingCard::get_Options
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
 - ITCallingCard::get_Options
 - tapi3if/ITCallingCard::get_Options
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
 - ITCallingCard.get_Options
---

# ITCallingCard::get_Options


## -description

The 
<b>get_Options</b> method gets the translation options for this address and card.

## -parameters

### -param plOptions [out]

Pointer to 
<a href="/windows/desktop/Tapi/linetranslateoption--constants">LINETRANSLATEOPTION</a> flags.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plOptions</i> parameter is not a valid pointer.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard">ITCallingCard</a>