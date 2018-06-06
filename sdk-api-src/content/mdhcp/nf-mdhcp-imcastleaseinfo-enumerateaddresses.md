---
UID: NF:mdhcp.IMcastLeaseInfo.EnumerateAddresses
title: IMcastLeaseInfo::EnumerateAddresses
author: windows-sdk-content
description: The EnumerateAddresses method obtains the collection of multicast addresses that are the subject of this lease or lease request. This method is primarily for C++ programmers. Visual Basic and other scripting languages use get_Addresses instead.
old-location: tapi3\imcastleaseinfo_enumerateaddresses.htm
old-project: Tapi
ms.assetid: edbfe386-9b3d-4160-916e-6c9ea640cfbc
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: EnumerateAddresses, EnumerateAddresses method [TAPI 2.2], EnumerateAddresses method [TAPI 2.2],IMcastLeaseInfo interface, IMcastLeaseInfo interface [TAPI 2.2],EnumerateAddresses method, IMcastLeaseInfo.EnumerateAddresses, IMcastLeaseInfo::EnumerateAddresses, _tapi3_imcastleaseinfo_enumerateaddresses, mdhcp/IMcastLeaseInfo::EnumerateAddresses, tapi3.imcastleaseinfo_enumerateaddresses
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
 - IMcastLeaseInfo.EnumerateAddresses
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Mdhcp.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMcastLeaseInfo::EnumerateAddresses


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>EnumerateAddresses</b> method obtains the collection of multicast addresses that are the subject of this lease or lease request. This method is primarily for C++ programmers. Visual Basic and other scripting languages use 
<a href="https://msdn.microsoft.com/37dc1bc8-b3d9-4c84-8d37-89d50570d95c">get_Addresses</a> instead.


## -parameters




### -param ppEnumAddresses [out]

Returns a pointer to a new 
<a href="https://msdn.microsoft.com/0e87ec06-7f3a-410c-9d54-7a67991e089c">IEnumBstr</a> object. 
<b>IEnumBstr</b> is a standard enumerator interface that enumerates BSTR strings. Each string is an IP version 4 address in dotted quad notation (for example, 10.111.222.111).


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
Not enough memory to allocate the enumerator.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/0e87ec06-7f3a-410c-9d54-7a67991e089c">IEnumBstr</a> interface returned by <b>IMcastLeaseInfo::EnumerateAddresses</b>. The application must call <b>Release</b> on the 
<b>IEnumBstr</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/0e87ec06-7f3a-410c-9d54-7a67991e089c">IEnumBstr</a>



<a href="https://msdn.microsoft.com/a4ad8009-559e-4db9-9ae2-28e4d36cf346">IMcastLeaseInfo</a>



<a href="https://msdn.microsoft.com/37dc1bc8-b3d9-4c84-8d37-89d50570d95c">get_Addresses</a>
 

 

