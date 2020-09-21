---
UID: NF:tapi3if.ITBasicCallControl.Disconnect
title: ITBasicCallControl::Disconnect (tapi3if.h)
description: The Disconnect method disconnects the call. The call state will transition to CS_DISCONNECTED after the method completes successfully.
helpviewer_keywords: ["Disconnect","Disconnect method [TAPI 2.2]","Disconnect method [TAPI 2.2]","ITBasicCallControl interface","ITBasicCallControl interface [TAPI 2.2]","Disconnect method","ITBasicCallControl.Disconnect","ITBasicCallControl::Disconnect","_tapi3_itbasiccallcontrol_disconnect","tapi3.itbasiccallcontrol_disconnect","tapi3if/ITBasicCallControl::Disconnect"]
old-location: tapi3\itbasiccallcontrol_disconnect.htm
tech.root: tapi3
ms.assetid: b7d556fd-d3f5-4b93-96a9-cc5c58fb8a95
ms.date: 12/05/2018
ms.keywords: Disconnect, Disconnect method [TAPI 2.2], Disconnect method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],Disconnect method, ITBasicCallControl.Disconnect, ITBasicCallControl::Disconnect, _tapi3_itbasiccallcontrol_disconnect, tapi3.itbasiccallcontrol_disconnect, tapi3if/ITBasicCallControl::Disconnect
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
 - ITBasicCallControl::Disconnect
 - tapi3if/ITBasicCallControl::Disconnect
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
 - ITBasicCallControl.Disconnect
---

# ITBasicCallControl::Disconnect


## -description

The 
<b>Disconnect</b> method disconnects the call. The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state">call state</a> will transition to CS_DISCONNECTED after the method completes successfully.

## -parameters

### -param code [in]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-disconnect_code">DISCONNECT_CODE</a> indicating reason for call disconnection.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The call state is CS_IDLE or a valid handle for the call could not be obtained by the TAPI 3 DLL.

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

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-disconnect_code">DISCONNECT_CODE</a>



<a href="/windows/desktop/Tapi/drop-ovr">Drop overview</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/Tapi/terminate-a-session-ovr">Terminate a Session Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a>