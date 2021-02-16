---
UID: NF:tapi3if.ITBasicCallControl.Transfer
title: ITBasicCallControl::Transfer (tapi3if.h)
description: The Transfer method transfers the current call to the destination address.
helpviewer_keywords: ["ITBasicCallControl interface [TAPI 2.2]","Transfer method","ITBasicCallControl.Transfer","ITBasicCallControl::Transfer","Transfer","Transfer method [TAPI 2.2]","Transfer method [TAPI 2.2]","ITBasicCallControl interface","_tapi3_itbasiccallcontrol_transfer","tapi3.itbasiccallcontrol_transfer","tapi3if/ITBasicCallControl::Transfer"]
old-location: tapi3\itbasiccallcontrol_transfer.htm
tech.root: tapi3
ms.assetid: 4f2a06e6-9f0b-4bf3-9f18-6e9f57c4b02f
ms.date: 12/05/2018
ms.keywords: ITBasicCallControl interface [TAPI 2.2],Transfer method, ITBasicCallControl.Transfer, ITBasicCallControl::Transfer, Transfer, Transfer method [TAPI 2.2], Transfer method [TAPI 2.2],ITBasicCallControl interface, _tapi3_itbasiccallcontrol_transfer, tapi3.itbasiccallcontrol_transfer, tapi3if/ITBasicCallControl::Transfer
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
 - ITBasicCallControl::Transfer
 - tapi3if/ITBasicCallControl::Transfer
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
 - ITBasicCallControl.Transfer
---

# ITBasicCallControl::Transfer


## -description

The 
<b>Transfer</b> method transfers the current call to the destination address.

## -parameters

### -param pCall [in]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a> interface of consultation call created for the transfer.

### -param fSync [in]

Indicates whether the method should be completed synchronously (VARIANT_TRUE) or asynchronously (VARIANT_FALSE).

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
The <i>pCall</i> parameter does not point to a valid call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Transfers not supported.

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

Some service providers do not support this operation while streaming is active. The application may need to call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-stopstream">ITStream::StopStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-stopsubstream">ITSubStream::StopSubStream</a> prior to the operation and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-startstream">ITStream::StartStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-startsubstream">ITSubStream::StartSubStream</a> following completion of the operation.

Call transfer involves setting up a consultation call in preparation for the transfer. <i>pCall</i> is the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a> pointer returned by 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a> following the creation of a consultation call. 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish">ITBasicCallControl::Finish</a> (FM_ASTRANSFER) completes the transfer.

If the consultation call is not in the CONNECTED state when 
<b>Transfer</b> is called, TAPI will use the destination address (as specified when the consultation call was first created via 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a>) and try to connect at that time. If the original call had a <b>NULL</b> destination address, 
<b>Transfer</b> will fail with E_INVALIDARG.

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-conference">Conference</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish">Finish</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/Tapi/transfer-ovr">Transfer Overview</a>