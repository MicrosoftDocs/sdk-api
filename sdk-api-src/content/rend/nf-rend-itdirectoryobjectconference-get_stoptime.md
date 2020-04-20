---
UID: NF:rend.ITDirectoryObjectConference.get_StopTime
title: ITDirectoryObjectConference::get_StopTime (rend.h)
description: The get_StopTime method gets the stop time of the conference. If the end time is zero, the session is not bounded.helpviewer_keywords: ["ITDirectoryObjectConference interface [TAPI 2.2]","get_StopTime method","ITDirectoryObjectConference.get_StopTime","ITDirectoryObjectConference::get_StopTime","_tapi3_itdirectoryobjectconference_get_stoptime","get_StopTime","get_StopTime method [TAPI 2.2]","get_StopTime method [TAPI 2.2]","ITDirectoryObjectConference interface","rend/ITDirectoryObjectConference::get_StopTime","tapi3.itdirectoryobjectconference_get_stoptime"]
old-location: tapi3\itdirectoryobjectconference_get_stoptime.htm
tech.root: Tapi
ms.assetid: df22b117-8382-4ea2-8e6b-961f87f41b21
ms.date: 12/05/2018
ms.keywords: ITDirectoryObjectConference interface [TAPI 2.2],get_StopTime method, ITDirectoryObjectConference.get_StopTime, ITDirectoryObjectConference::get_StopTime, _tapi3_itdirectoryobjectconference_get_stoptime, get_StopTime, get_StopTime method [TAPI 2.2], get_StopTime method [TAPI 2.2],ITDirectoryObjectConference interface, rend/ITDirectoryObjectConference::get_StopTime, tapi3.itdirectoryobjectconference_get_stoptime
f1_keywords:
- rend/ITDirectoryObjectConference.get_StopTime
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Rend.dll
api_name:
- ITDirectoryObjectConference.get_StopTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITDirectoryObjectConference::get_StopTime


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_StopTime</b> method gets the stop time of the conference. If the end time is zero, the session is not bounded.


## -parameters




### -param pDate [out]

Pointer to the conference stop time.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pDate</i> parameter is not a valid pointer.

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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rend/nn-rend-itdirectoryobjectconference">ITDirectoryObjectConference</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-put_stoptime">ITDirectoryObjectConference::put_StopTime</a>
 

 

