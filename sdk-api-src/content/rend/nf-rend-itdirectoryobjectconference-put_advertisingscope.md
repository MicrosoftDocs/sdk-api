---
UID: NF:rend.ITDirectoryObjectConference.put_AdvertisingScope
title: ITDirectoryObjectConference::put_AdvertisingScope
author: windows-sdk-content
description: The put_AdvertisingScope method sets the advertising scope.
old-location: tapi3\itdirectoryobjectconference_put_advertisingscope.htm
old-project: tapi
ms.assetid: 74d7c770-e11d-4d87-acdb-821d64feed0c
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITDirectoryObjectConference interface [TAPI 2.2],put_AdvertisingScope method, ITDirectoryObjectConference.put_AdvertisingScope, ITDirectoryObjectConference::put_AdvertisingScope, _tapi3_itdirectoryobjectconference_put_advertisingscope, put_AdvertisingScope, put_AdvertisingScope method [TAPI 2.2], put_AdvertisingScope method [TAPI 2.2],ITDirectoryObjectConference interface, rend/ITDirectoryObjectConference::put_AdvertisingScope, tapi3.itdirectoryobjectconference_put_advertisingscope
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
 - ITDirectoryObjectConference.put_AdvertisingScope
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: ADAM
---

# ITDirectoryObjectConference::put_AdvertisingScope


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>put_AdvertisingScope</b> method sets the advertising scope.


## -parameters




### -param AdvertisingScope [in]

Pointer to 
<a href="https://msdn.microsoft.com/e08e7b8a-e27b-48a8-ab2d-d4ce5fed912a">RND_ADVERTISING_SCOPE</a> enumeration.


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
The <i>AdvertisingScope</i> parameter is not valid.

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



<a href="https://msdn.microsoft.com/25e155ad-c809-4ff4-85cb-ca43cb203368">ITDirectoryObjectConference::get_AdvertisingScope</a>



<a href="https://msdn.microsoft.com/e08e7b8a-e27b-48a8-ab2d-d4ce5fed912a">RND_ADVERTISING_SCOPE</a>
 

 

