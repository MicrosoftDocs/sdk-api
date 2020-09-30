---
UID: NF:tapi3if.ITAddress.put_MessageWaiting
title: ITAddress::put_MessageWaiting (tapi3if.h)
description: The put_MessageWaiting method sets the status of the message waiting on the address.
helpviewer_keywords: ["ITAddress interface [TAPI 2.2]","put_MessageWaiting method","ITAddress.put_MessageWaiting","ITAddress::put_MessageWaiting","_tapi3_itaddress_put_messagewaiting","put_MessageWaiting","put_MessageWaiting method [TAPI 2.2]","put_MessageWaiting method [TAPI 2.2]","ITAddress interface","tapi3.itaddress_put_messagewaiting","tapi3if/ITAddress::put_MessageWaiting"]
old-location: tapi3\itaddress_put_messagewaiting.htm
tech.root: tapi3
ms.assetid: 9dc125ab-a452-4108-93d5-9f341b879e8d
ms.date: 12/05/2018
ms.keywords: ITAddress interface [TAPI 2.2],put_MessageWaiting method, ITAddress.put_MessageWaiting, ITAddress::put_MessageWaiting, _tapi3_itaddress_put_messagewaiting, put_MessageWaiting, put_MessageWaiting method [TAPI 2.2], put_MessageWaiting method [TAPI 2.2],ITAddress interface, tapi3.itaddress_put_messagewaiting, tapi3if/ITAddress::put_MessageWaiting
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
 - ITAddress::put_MessageWaiting
 - tapi3if/ITAddress::put_MessageWaiting
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
 - ITAddress.put_MessageWaiting
---

# ITAddress::put_MessageWaiting


## -description

The 
<b>put_MessageWaiting</b> method sets the status of the message waiting on the address.

## -parameters

### -param fMessageWaiting [in]

Status of message waiting to be set.

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
The <i>fMessageWaiting</i> parameter is not valid.

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
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>

## -remarks

For programmers familiar with TAPI 2.<i>x:</i> This method turns on and off the flag LINEDEVSTATUSFLAGS_MSGWAIT in the <b>dwDevStatusFlags</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a> structure by calling 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetlinedevstatus">lineSetLineDevStatus</a>.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_messagewaiting">get_MessageWaiting</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetlinedevstatus">lineSetLineDevStatus</a>