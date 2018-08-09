---
UID: NF:mdhcp.IMcastLeaseInfo.get_ServerAddress
title: IMcastLeaseInfo::get_ServerAddress
author: windows-sdk-content
description: The get_ServerAddress method obtains a string representing the address of the multicast server granting this lease.
old-location: tapi3\imcastleaseinfo_get_serveraddress.htm
old-project: tapi
ms.assetid: 15f33689-07d5-4bd9-978a-2b5d9088b2ed
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: IMcastLeaseInfo interface [TAPI 2.2],get_ServerAddress method, IMcastLeaseInfo.get_ServerAddress, IMcastLeaseInfo::get_ServerAddress, _tapi3_imcastleaseinfo_get_serveraddress, get_ServerAddress, get_ServerAddress method [TAPI 2.2], get_ServerAddress method [TAPI 2.2],IMcastLeaseInfo interface, mdhcp/IMcastLeaseInfo::get_ServerAddress, tapi3.imcastleaseinfo_get_serveraddress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mdhcp.h
req.include-header: 
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
tech.root: 
req.typenames: MODEMSETTINGS, *PMODEMSETTINGS, *LPMODEMSETTINGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mdhcp.dll
api_name:
 - IMcastLeaseInfo.get_ServerAddress
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Mdhcp.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMcastLeaseInfo::get_ServerAddress


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>get_ServerAddress</b> method obtains a string representing the address of the multicast server granting this lease.


## -parameters




### -param ppAddress [out]

Pointer to a <b>BSTR</b> that will receive a string representation of the address of the server granting this request or renewal.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Server address unspecified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The caller passed in an invalid pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory exists to allocate the string.

</td>
</tr>
</table>
 




## -remarks



The <b>BSTR</b> string <i>ppAddress</i> is an IP version 4 address in dotted quad notation (for example, 10.111.222.111). If a lease information object does not describe a granted lease (for example, it was not returned by 
<a href="https://msdn.microsoft.com/ca428138-34d2-499d-9560-8dfd51403ba1">IMcastAddressAllocation::RequestAddress</a> or 
<a href="https://msdn.microsoft.com/9f52d1e9-61d9-4f67-b180-c1844b4eb7f1">IMcastAddressAllocation::RenewAddress</a>), the address is reported as the string "Unspecified".

The application must use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>ppAddress</i> parameter.
			

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.




## -see-also




<a href="https://msdn.microsoft.com/a4ad8009-559e-4db9-9ae2-28e4d36cf346">IMcastLeaseInfo</a>
 

 

