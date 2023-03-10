---
UID: NF:tapi3if.ITBasicCallControl.Finish
title: ITBasicCallControl::Finish (tapi3if.h)
description: The Finish method is called on a consultation call to finish a conference or a transfer.
helpviewer_keywords: ["Finish","Finish method [TAPI 2.2]","Finish method [TAPI 2.2]","ITBasicCallControl interface","ITBasicCallControl interface [TAPI 2.2]","Finish method","ITBasicCallControl.Finish","ITBasicCallControl::Finish","_tapi3_itbasiccallcontrol_finish","tapi3.itbasiccallcontrol_finish","tapi3if/ITBasicCallControl::Finish"]
old-location: tapi3\itbasiccallcontrol_finish.htm
tech.root: tapi3
ms.assetid: 3b0bd871-b618-4c24-a717-62a248112d97
ms.date: 12/05/2018
ms.keywords: Finish, Finish method [TAPI 2.2], Finish method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],Finish method, ITBasicCallControl.Finish, ITBasicCallControl::Finish, _tapi3_itbasiccallcontrol_finish, tapi3.itbasiccallcontrol_finish, tapi3if/ITBasicCallControl::Finish
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
 - ITBasicCallControl::Finish
 - tapi3if/ITBasicCallControl::Finish
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
 - ITBasicCallControl.Finish
---

# ITBasicCallControl::Finish


## -description

The 
<b>Finish</b> method is called on a consultation call to finish a conference or a transfer.

## -parameters

### -param finishMode [in]

A 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-finish_mode">FINISH_MODE</a> indicator of the type of call being finished, such as FM_ASCONFERENCE.

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
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
Call is not flagged as a transfer or a conference.

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

## -remarks

Some service providers do not support this operation while streaming is active. The application may need to call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-stopstream">ITStream::StopStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-stopsubstream">ITSubStream::StopSubStream</a> prior to the operation and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-startstream">ITStream::StartStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-startsubstream">ITSubStream::StartSubStream</a> following completion of the operation.

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-conference">Conference</a>



<a href="/windows/desktop/Tapi/conference-ovr">Conference overview</a>



<a href="/windows/desktop/Tapi/create-a-simple-conference">Create a Simple Conference code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-finish_mode">FINISH_MODE</a>



<a href="/windows/desktop/Tapi/forward-ovr">Forward overview</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer">Transfer</a>



<a href="/windows/desktop/Tapi/transfer-ovr">Transfer overview</a>