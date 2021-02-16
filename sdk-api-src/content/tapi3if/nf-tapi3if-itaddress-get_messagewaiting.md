---
UID: NF:tapi3if.ITAddress.get_MessageWaiting
title: ITAddress::get_MessageWaiting (tapi3if.h)
description: The get_MessageWaiting method determines if the address has a message waiting.
helpviewer_keywords: ["ITAddress interface [TAPI 2.2]","get_MessageWaiting method","ITAddress.get_MessageWaiting","ITAddress::get_MessageWaiting","_tapi3_itaddress_get_messagewaiting","get_MessageWaiting","get_MessageWaiting method [TAPI 2.2]","get_MessageWaiting method [TAPI 2.2]","ITAddress interface","tapi3.itaddress_get_messagewaiting","tapi3if/ITAddress::get_MessageWaiting"]
old-location: tapi3\itaddress_get_messagewaiting.htm
tech.root: tapi3
ms.assetid: 4ddb49d9-dde7-498b-a243-f8c5b1294a87
ms.date: 12/05/2018
ms.keywords: ITAddress interface [TAPI 2.2],get_MessageWaiting method, ITAddress.get_MessageWaiting, ITAddress::get_MessageWaiting, _tapi3_itaddress_get_messagewaiting, get_MessageWaiting, get_MessageWaiting method [TAPI 2.2], get_MessageWaiting method [TAPI 2.2],ITAddress interface, tapi3.itaddress_get_messagewaiting, tapi3if/ITAddress::get_MessageWaiting
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
 - ITAddress::get_MessageWaiting
 - tapi3if/ITAddress::get_MessageWaiting
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
 - ITAddress.get_MessageWaiting
---

# ITAddress::get_MessageWaiting


## -description

The 
<b>get_MessageWaiting</b> method determines if the address has a message waiting.

## -parameters

### -param pfMessageWaiting [out]

If VARIANT_TRUE is returned, a message is waiting; if VARIANT_FALSE is returned, no message is waiting.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pfMessageWaiting</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

In TAPI 2.<i>x</i>, this maps to the flag LINEDEVSTATUSFLAGS_MSGWAIT being set or not in the member <i>dwDevStatusFlags</i> from the structure 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a>.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-put_messagewaiting">put_MessageWaiting</a>