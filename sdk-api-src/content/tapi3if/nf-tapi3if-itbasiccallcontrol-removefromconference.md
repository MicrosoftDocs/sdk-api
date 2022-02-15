---
UID: NF:tapi3if.ITBasicCallControl.RemoveFromConference
title: ITBasicCallControl::RemoveFromConference (tapi3if.h)
description: The RemoveFromConference method removes the call from a conference if it is involved in one.
helpviewer_keywords: ["ITBasicCallControl interface [TAPI 2.2]","RemoveFromConference method","ITBasicCallControl.RemoveFromConference","ITBasicCallControl::RemoveFromConference","RemoveFromConference","RemoveFromConference method [TAPI 2.2]","RemoveFromConference method [TAPI 2.2]","ITBasicCallControl interface","_tapi3_itbasiccallcontrol_removefromconference","tapi3.itbasiccallcontrol_removefromconference","tapi3if/ITBasicCallControl::RemoveFromConference"]
old-location: tapi3\itbasiccallcontrol_removefromconference.htm
tech.root: tapi3
ms.assetid: c3a357a1-9bfa-4d23-b7d7-e1d9b636e861
ms.date: 12/05/2018
ms.keywords: ITBasicCallControl interface [TAPI 2.2],RemoveFromConference method, ITBasicCallControl.RemoveFromConference, ITBasicCallControl::RemoveFromConference, RemoveFromConference, RemoveFromConference method [TAPI 2.2], RemoveFromConference method [TAPI 2.2],ITBasicCallControl interface, _tapi3_itbasiccallcontrol_removefromconference, tapi3.itbasiccallcontrol_removefromconference, tapi3if/ITBasicCallControl::RemoveFromConference
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
 - ITBasicCallControl::RemoveFromConference
 - tapi3if/ITBasicCallControl::RemoveFromConference
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
 - ITBasicCallControl.RemoveFromConference
---

# ITBasicCallControl::RemoveFromConference


## -description

The 
<b>RemoveFromConference</b> method removes the call from a conference if it is involved in one.



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

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/Tapi/conference-ovr">Conference overview</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineremovefromconference">lineRemoveFromConference</a>
