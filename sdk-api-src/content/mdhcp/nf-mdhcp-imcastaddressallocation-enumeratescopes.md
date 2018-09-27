---
UID: NF:mdhcp.IMcastAddressAllocation.EnumerateScopes
title: IMcastAddressAllocation::EnumerateScopes
author: windows-sdk-content
description: The EnumerateScopes method creates an enumeration of multicast scopes available. This method is primarily for C++ programmers. Visual Basic and other scripting languages use get_Scopes instead.
old-location: tapi3\imcastaddressallocation_enumeratescopes.htm
tech.root: tapi
ms.assetid: 1845f5f9-be0e-4609-89d8-1a0ed194dd68
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: EnumerateScopes, EnumerateScopes method [TAPI 2.2], EnumerateScopes method [TAPI 2.2],IMcastAddressAllocation interface, IMcastAddressAllocation interface [TAPI 2.2],EnumerateScopes method, IMcastAddressAllocation.EnumerateScopes, IMcastAddressAllocation::EnumerateScopes, _tapi3_imcastaddressallocation_enumeratescopes, mdhcp/IMcastAddressAllocation::EnumerateScopes, tapi3.imcastaddressallocation_enumeratescopes
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Uuid.lib
req.dll: Mdhcp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mdhcp.dll
api_name:
 - IMcastAddressAllocation.EnumerateScopes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMcastAddressAllocation::EnumerateScopes


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>EnumerateScopes</b> method creates an enumeration of multicast scopes available. This method is primarily for C++ programmers. Visual Basic and other scripting languages use 
<a href="https://msdn.microsoft.com/4fe824fa-2fcb-4f6b-b3de-15dcfc79575c">get_Scopes</a> instead.


## -parameters




### -param ppEnumMcastScope [out]

Returns a pointer to a new 
<a href="https://msdn.microsoft.com/edc8be8e-635b-43f3-a4c1-7566e354cc3e">IEnumMcastScope</a> object.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There are no scopes available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory exists to create the required objects.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/edc8be8e-635b-43f3-a4c1-7566e354cc3e">IEnumMcastScope</a> interface returned by <b>IMcastAddressAllocation::EnumerateScopes</b>. The application must call <b>Release</b> on the 
<b>IEnumMcastScope</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/359e67bb-9a5b-4caa-8d3b-eb0739b0828f">IMcastAddressAllocation</a>
 

 

