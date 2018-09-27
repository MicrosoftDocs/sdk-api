---
UID: NF:mdhcp.IMcastScope.get_ServerID
title: IMcastScope::get_ServerID
author: windows-sdk-content
description: The get_ServerID method obtains the server ID associated with this scope.
old-location: tapi3\imcastscope_get_serverid.htm
tech.root: tapi
ms.assetid: 80c0ecca-647f-4e5e-92d6-fc95368715ad
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IMcastScope interface [TAPI 2.2],get_ServerID method, IMcastScope.get_ServerID, IMcastScope::get_ServerID, _tapi3_imcastscope_get_serverid, get_ServerID, get_ServerID method [TAPI 2.2], get_ServerID method [TAPI 2.2],IMcastScope interface, mdhcp/IMcastScope::get_ServerID, tapi3.imcastscope_get_serverid
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
 - IMcastScope.get_ServerID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMcastScope::get_ServerID


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_ServerID</b> method obtains the server ID associated with this scope. The scope ID and server ID are needed to select this scope in subsequent calls to 
<a href="https://msdn.microsoft.com/ca428138-34d2-499d-9560-8dfd51403ba1">IMcastAddressAllocation::RequestAddress</a>, 
<a href="https://msdn.microsoft.com/9f52d1e9-61d9-4f67-b180-c1844b4eb7f1">IMcastAddressAllocation::RenewAddress</a>, or 
<a href="https://msdn.microsoft.com/6b5fd18b-1b13-4e2a-9ff9-4a66212213a7">IMcastAddressAllocation::ReleaseAddress</a>.


## -parameters




### -param pID [out]

Pointer to a <b>LONG</b> that will receive the server ID of this scope, which is the ID that was assigned to the multicast address allocation server that published this scope at the time that the server was configured.


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
The caller passed in an invalid pointer argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b0252ac4-856e-4aa7-aa3b-37b92472e864">IMcastScope</a>



<a href="https://msdn.microsoft.com/9c0ba8ab-1022-40c6-9d89-74250c149681">IMcastScope::get_ScopeID</a>
 

 

