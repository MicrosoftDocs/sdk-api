---
UID: NF:rend.ITDirectoryObjectConference.get_Protocol
title: ITDirectoryObjectConference::get_Protocol
author: windows-driver-content
description: The get_Protocol method gets protocol identification.
old-location: tapi3\itdirectoryobjectconference_get_protocol.htm
old-project: Tapi
ms.assetid: 2a9d1b8e-1ebc-4a67-87cf-f88aaf25c309
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: ITDirectoryObjectConference interface [TAPI 2.2],get_Protocol method, ITDirectoryObjectConference.get_Protocol, ITDirectoryObjectConference::get_Protocol, _tapi3_itdirectoryobjectconference_get_protocol, get_Protocol, get_Protocol method [TAPI 2.2], get_Protocol method [TAPI 2.2],ITDirectoryObjectConference interface, rend/ITDirectoryObjectConference::get_Protocol, tapi3.itdirectoryobjectconference_get_protocol
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
-	ITDirectoryObjectConference.get_Protocol
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITDirectoryObjectConference::get_Protocol


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_Protocol</b> method gets protocol identification.


## -parameters




### -param ppProtocol [out]

Pointer to a <b>BSTR</b> containing the protocol identifier.


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
The <i>ppProtocol</i> parameter is not a valid pointer.

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



The application must use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>ppProtocol</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/bab167cf-2726-4423-87b3-69227404bddc">ITDirectoryObjectConference</a>
 

 

