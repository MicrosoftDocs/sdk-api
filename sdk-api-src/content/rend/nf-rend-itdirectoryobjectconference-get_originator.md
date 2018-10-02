---
UID: NF:rend.ITDirectoryObjectConference.get_Originator
title: ITDirectoryObjectConference::get_Originator
author: windows-sdk-content
description: The get_Originator method gets the originator's user name.
old-location: tapi3\itdirectoryobjectconference_get_originator.htm
tech.root: TAPI
ms.assetid: b17be92c-eee6-43ec-bec0-75d4c30ad22f
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITDirectoryObjectConference interface [TAPI 2.2],get_Originator method, ITDirectoryObjectConference.get_Originator, ITDirectoryObjectConference::get_Originator, _tapi3_itdirectoryobjectconference_get_originator, get_Originator, get_Originator method [TAPI 2.2], get_Originator method [TAPI 2.2],ITDirectoryObjectConference interface, rend/ITDirectoryObjectConference::get_Originator, tapi3.itdirectoryobjectconference_get_originator
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
 - ITDirectoryObjectConference.get_Originator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDirectoryObjectConference::get_Originator


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_Originator</b> method gets the originator's user name.


## -parameters




### -param ppOriginator [out]

Pointer to a <b>BSTR</b> containing the originator's user name.


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
The <i>ppOriginator</i> parameter is not a valid pointer.

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
<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory allocated for the <i>ppOriginator</i> parameter.

The originator's name, along with the machine name set in 
<a href="https://msdn.microsoft.com/f4af55b1-e20b-4fe8-a15e-a1a68d22f1b9">put_MachineAddress</a>, are collectively the originator of the conference, and both are in the o= line of the SDP.




## -see-also




<a href="https://msdn.microsoft.com/bab167cf-2726-4423-87b3-69227404bddc">ITDirectoryObjectConference</a>



<a href="https://msdn.microsoft.com/97e8b966-b65c-4c19-ac61-0b952657aec1">ITDirectoryObjectConference::put_Originator</a>
 

 

