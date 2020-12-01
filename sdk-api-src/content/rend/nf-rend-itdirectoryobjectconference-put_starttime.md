---
UID: NF:rend.ITDirectoryObjectConference.put_StartTime
title: ITDirectoryObjectConference::put_StartTime (rend.h)
description: The put_StartTime method sets the start time of the conference.
helpviewer_keywords: ["ITDirectoryObjectConference interface [TAPI 2.2]","put_StartTime method","ITDirectoryObjectConference.put_StartTime","ITDirectoryObjectConference::put_StartTime","_tapi3_itdirectoryobjectconference_put_starttime","put_StartTime","put_StartTime method [TAPI 2.2]","put_StartTime method [TAPI 2.2]","ITDirectoryObjectConference interface","rend/ITDirectoryObjectConference::put_StartTime","tapi3.itdirectoryobjectconference_put_starttime"]
old-location: tapi3\itdirectoryobjectconference_put_starttime.htm
tech.root: tapi3
ms.assetid: 87ccf59c-3fe6-4247-b7f9-d1fb8bcf4b69
ms.date: 12/05/2018
ms.keywords: ITDirectoryObjectConference interface [TAPI 2.2],put_StartTime method, ITDirectoryObjectConference.put_StartTime, ITDirectoryObjectConference::put_StartTime, _tapi3_itdirectoryobjectconference_put_starttime, put_StartTime, put_StartTime method [TAPI 2.2], put_StartTime method [TAPI 2.2],ITDirectoryObjectConference interface, rend/ITDirectoryObjectConference::put_StartTime, tapi3.itdirectoryobjectconference_put_starttime
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
 - ITDirectoryObjectConference::put_StartTime
 - rend/ITDirectoryObjectConference::put_StartTime
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
 - ITDirectoryObjectConference.put_StartTime
---

# ITDirectoryObjectConference::put_StartTime


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>put_StartTime</b> method sets the start time of the conference.

## -parameters

### -param Date [in]

Conference start time.

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

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobjectconference">ITDirectoryObjectConference</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-get_starttime">ITDirectoryObjectConference::get_StartTime</a>