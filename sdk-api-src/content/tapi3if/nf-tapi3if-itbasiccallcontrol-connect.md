---
UID: NF:tapi3if.ITBasicCallControl.Connect
title: ITBasicCallControl::Connect (tapi3if.h)
description: The Connect method attempts to complete the connection of an outgoing call.
helpviewer_keywords: ["Connect","Connect method [TAPI 2.2]","Connect method [TAPI 2.2]","ITBasicCallControl interface","ITBasicCallControl interface [TAPI 2.2]","Connect method","ITBasicCallControl.Connect","ITBasicCallControl::Connect","_tapi3_itbasiccallcontrol_connect","tapi3.itbasiccallcontrol_connect","tapi3if/ITBasicCallControl::Connect"]
old-location: tapi3\itbasiccallcontrol_connect.htm
tech.root: tapi3
ms.assetid: cc9a8bfd-14c0-459c-a911-325b73323c08
ms.date: 12/05/2018
ms.keywords: Connect, Connect method [TAPI 2.2], Connect method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],Connect method, ITBasicCallControl.Connect, ITBasicCallControl::Connect, _tapi3_itbasiccallcontrol_connect, tapi3.itbasiccallcontrol_connect, tapi3if/ITBasicCallControl::Connect
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
 - ITBasicCallControl::Connect
 - tapi3if/ITBasicCallControl::Connect
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
 - ITBasicCallControl.Connect
---

# ITBasicCallControl::Connect


## -description

The 
<b>Connect</b> method attempts to complete the connection of an outgoing call.

## -parameters

### -param fSync [in]

Boolean indicating whether connection is to be performed synchronously (VARIANT_TRUE) or asynchronously (VARIANT_FALSE).

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

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state">Call state</a> must be CS_IDLE.

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

If the call is asynchronous, the application will receive information about the call's progress through the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent">ITCallNotificationEvent</a> outgoing interface. The application must register the outgoing interface before calling 
<b>Connect</b>. 
<b>Connect</b> may return S_OK, but the actual connection may fail (and the application will be notified through the outgoing interface).

If the call is synchronous, this method will not return until the call is in the connected state or fails.

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/Tapi/complete-a-session-ovr">Complete a Session</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>