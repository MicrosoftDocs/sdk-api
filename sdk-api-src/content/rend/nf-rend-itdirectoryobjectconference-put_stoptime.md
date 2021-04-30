---
UID: NF:rend.ITDirectoryObjectConference.put_StopTime
title: ITDirectoryObjectConference::put_StopTime (rend.h)
description: The put_StopTime method sets the stop time of the conference. If the end time is zero, the session is not bounded.
helpviewer_keywords: ["ITDirectoryObjectConference interface [TAPI 2.2]","put_StopTime method","ITDirectoryObjectConference.put_StopTime","ITDirectoryObjectConference::put_StopTime","_tapi3_itdirectoryobjectconference_put_stoptime","put_StopTime","put_StopTime method [TAPI 2.2]","put_StopTime method [TAPI 2.2]","ITDirectoryObjectConference interface","rend/ITDirectoryObjectConference::put_StopTime","tapi3.itdirectoryobjectconference_put_stoptime"]
old-location: tapi3\itdirectoryobjectconference_put_stoptime.htm
tech.root: tapi3
ms.assetid: 2542f3e2-d391-4d96-8aa8-120d639f0468
ms.date: 12/05/2018
ms.keywords: ITDirectoryObjectConference interface [TAPI 2.2],put_StopTime method, ITDirectoryObjectConference.put_StopTime, ITDirectoryObjectConference::put_StopTime, _tapi3_itdirectoryobjectconference_put_stoptime, put_StopTime, put_StopTime method [TAPI 2.2], put_StopTime method [TAPI 2.2],ITDirectoryObjectConference interface, rend/ITDirectoryObjectConference::put_StopTime, tapi3.itdirectoryobjectconference_put_stoptime
req.header: rend.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Rend.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITDirectoryObjectConference::put_StopTime
 - rend/ITDirectoryObjectConference::put_StopTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITDirectoryObjectConference.put_StopTime
---

# ITDirectoryObjectConference::put_StopTime


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>put_StopTime</b> method sets the stop time of the conference. If the end time is zero, the session is not bounded.

## -parameters

### -param Date [in]

Conference stop time.

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
The <i>Date</i> parameter is not valid.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not yet implemented.

</td>
</tr>
</table>

## -remarks

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobjectconference">ITDirectoryObjectConference</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-get_stoptime">ITDirectoryObjectConference::get_StopTime</a>