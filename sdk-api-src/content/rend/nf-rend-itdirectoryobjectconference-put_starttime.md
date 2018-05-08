---
UID: NF:rend.ITDirectoryObjectConference.put_StartTime
title: ITDirectoryObjectConference::put_StartTime
author: windows-driver-content
description: The put_StartTime method sets the start time of the conference.
old-location: tapi3\itdirectoryobjectconference_put_starttime.htm
old-project: Tapi
ms.assetid: 87ccf59c-3fe6-4247-b7f9-d1fb8bcf4b69
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITDirectoryObjectConference interface [TAPI 2.2],put_StartTime method, ITDirectoryObjectConference.put_StartTime, ITDirectoryObjectConference::put_StartTime, _tapi3_itdirectoryobjectconference_put_starttime, put_StartTime, put_StartTime method [TAPI 2.2], put_StartTime method [TAPI 2.2],ITDirectoryObjectConference interface, rend/ITDirectoryObjectConference::put_StartTime, tapi3.itdirectoryobjectconference_put_starttime
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: RND_ADVERTISING_SCOPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Rend.dll
api_name:
-	ITDirectoryObjectConference.put_StartTime
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITDirectoryObjectConference::put_StartTime


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
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




<a href="https://msdn.microsoft.com/bab167cf-2726-4423-87b3-69227404bddc">ITDirectoryObjectConference</a>



<a href="https://msdn.microsoft.com/aeb496d5-2cea-4c69-ba19-c9083d133c1e">ITDirectoryObjectConference::get_StartTime</a>
 

 

