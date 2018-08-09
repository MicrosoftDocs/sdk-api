---
UID: NF:rend.ITDirectoryObjectConference.get_StopTime
title: ITDirectoryObjectConference::get_StopTime
author: windows-sdk-content
description: The get_StopTime method gets the stop time of the conference. If the end time is zero, the session is not bounded.
old-location: tapi3\itdirectoryobjectconference_get_stoptime.htm
old-project: tapi
ms.assetid: df22b117-8382-4ea2-8e6b-961f87f41b21
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITDirectoryObjectConference interface [TAPI 2.2],get_StopTime method, ITDirectoryObjectConference.get_StopTime, ITDirectoryObjectConference::get_StopTime, _tapi3_itdirectoryobjectconference_get_stoptime, get_StopTime, get_StopTime method [TAPI 2.2], get_StopTime method [TAPI 2.2],ITDirectoryObjectConference interface, rend/ITDirectoryObjectConference::get_StopTime, tapi3.itdirectoryobjectconference_get_stoptime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: RND_ADVERTISING_SCOPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITDirectoryObjectConference.get_StopTime
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: ADAM
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




<a href="https://msdn.microsoft.com/bab167cf-2726-4423-87b3-69227404bddc">ITDirectoryObjectConference</a>



<a href="https://msdn.microsoft.com/2542f3e2-d391-4d96-8aa8-120d639f0468">ITDirectoryObjectConference::put_StopTime</a>
 

 

