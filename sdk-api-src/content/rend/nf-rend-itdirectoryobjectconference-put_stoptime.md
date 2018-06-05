---
UID: NF:rend.ITDirectoryObjectConference.put_StopTime
title: ITDirectoryObjectConference::put_StopTime
author: windows-sdk-content
description: The put_StopTime method sets the stop time of the conference. If the end time is zero, the session is not bounded.
old-location: tapi3\itdirectoryobjectconference_put_stoptime.htm
old-project: Tapi
ms.assetid: 2542f3e2-d391-4d96-8aa8-120d639f0468
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITDirectoryObjectConference interface [TAPI 2.2],put_StopTime method, ITDirectoryObjectConference.put_StopTime, ITDirectoryObjectConference::put_StopTime, _tapi3_itdirectoryobjectconference_put_stoptime, put_StopTime, put_StopTime method [TAPI 2.2], put_StopTime method [TAPI 2.2],ITDirectoryObjectConference interface, rend/ITDirectoryObjectConference::put_StopTime, tapi3.itdirectoryobjectconference_put_stoptime
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Rend.dll
api_name:
-	ITDirectoryObjectConference.put_StopTime
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITDirectoryObjectConference::put_StopTime


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
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




<a href="https://msdn.microsoft.com/bab167cf-2726-4423-87b3-69227404bddc">ITDirectoryObjectConference</a>



<a href="https://msdn.microsoft.com/df22b117-8382-4ea2-8e6b-961f87f41b21">ITDirectoryObjectConference::get_StopTime</a>
 

 

