---
UID: NF:tapi3if.ITBasicCallControl.Hold
title: ITBasicCallControl::Hold (tapi3if.h)
description: The Hold method places or removes the call from the hold.
helpviewer_keywords: ["Hold","Hold method [TAPI 2.2]","Hold method [TAPI 2.2]","ITBasicCallControl interface","ITBasicCallControl interface [TAPI 2.2]","Hold method","ITBasicCallControl.Hold","ITBasicCallControl::Hold","_tapi3_itbasiccallcontrol_hold","tapi3.itbasiccallcontrol_hold","tapi3if/ITBasicCallControl::Hold"]
old-location: tapi3\itbasiccallcontrol_hold.htm
tech.root: tapi3
ms.assetid: 44f1d3fd-6c48-41f4-a30e-83bf2ce19fde
ms.date: 12/05/2018
ms.keywords: Hold, Hold method [TAPI 2.2], Hold method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],Hold method, ITBasicCallControl.Hold, ITBasicCallControl::Hold, _tapi3_itbasiccallcontrol_hold, tapi3.itbasiccallcontrol_hold, tapi3if/ITBasicCallControl::Hold
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
 - ITBasicCallControl::Hold
 - tapi3if/ITBasicCallControl::Hold
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
 - ITBasicCallControl.Hold
---

# ITBasicCallControl::Hold


## -description

The 
<b>Hold</b> method places or removes the call from the hold.

## -parameters

### -param fHold [in]

If <i>fHold</i> is VARIANT_TRUE and the method succeeds, the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state">call state</a> transitions to the CS_HOLD state. If <i>fHold</i> is VARIANT_FALSE, the call state transitions to CS_CONNECTED.

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
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
The call associated with this interface no longer exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes

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



<a href="/windows/desktop/Tapi/hold-ovr">Hold overview</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linehold">lineHold</a>