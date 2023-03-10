---
UID: NF:tapi3if.ITCallingCard.get_PermanentCardID
title: ITCallingCard::get_PermanentCardID (tapi3if.h)
description: The get_PermanentCardID method gets the permanent identifier that identifies the card.
helpviewer_keywords: ["ITCallingCard interface [TAPI 2.2]","get_PermanentCardID method","ITCallingCard.get_PermanentCardID","ITCallingCard::get_PermanentCardID","_tapi3_itcallingcard_get_permanentcardid","get_PermanentCardID","get_PermanentCardID method [TAPI 2.2]","get_PermanentCardID method [TAPI 2.2]","ITCallingCard interface","tapi3.itcallingcard_get_permanentcardid","tapi3if/ITCallingCard::get_PermanentCardID"]
old-location: tapi3\itcallingcard_get_permanentcardid.htm
tech.root: tapi3
ms.assetid: 75c37941-f950-4f86-be47-9aefe17995a5
ms.date: 12/05/2018
ms.keywords: ITCallingCard interface [TAPI 2.2],get_PermanentCardID method, ITCallingCard.get_PermanentCardID, ITCallingCard::get_PermanentCardID, _tapi3_itcallingcard_get_permanentcardid, get_PermanentCardID, get_PermanentCardID method [TAPI 2.2], get_PermanentCardID method [TAPI 2.2],ITCallingCard interface, tapi3.itcallingcard_get_permanentcardid, tapi3if/ITCallingCard::get_PermanentCardID
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
 - ITCallingCard::get_PermanentCardID
 - tapi3if/ITCallingCard::get_PermanentCardID
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
 - ITCallingCard.get_PermanentCardID
---

# ITCallingCard::get_PermanentCardID


## -description

The 
<b>get_PermanentCardID</b> method gets the permanent identifier that identifies the card.

## -parameters

### -param plCardID [out]

Pointer to calling card identifier.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>plCardID</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plCardID</i> parameter is not a valid pointer.

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