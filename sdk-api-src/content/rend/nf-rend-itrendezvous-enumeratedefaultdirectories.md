---
UID: NF:rend.ITRendezvous.EnumerateDefaultDirectories
title: ITRendezvous::EnumerateDefaultDirectories
author: windows-sdk-content
description: The EnumerateDefaultDirectories method enumerates all configured default directories. This method is similar to get_DefaultDirectories but is designed for C/C++.
old-location: tapi3\itrendezvous_enumeratedefaultdirectories.htm
tech.root: tapi
ms.assetid: fe89a370-32ed-4519-bb98-9d9ea7615eb7
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: EnumerateDefaultDirectories, EnumerateDefaultDirectories method [TAPI 2.2], EnumerateDefaultDirectories method [TAPI 2.2],ITRendezvous interface, ITRendezvous interface [TAPI 2.2],EnumerateDefaultDirectories method, ITRendezvous.EnumerateDefaultDirectories, ITRendezvous::EnumerateDefaultDirectories, _tapi3_itrendezvous_enumeratedefaultdirectories, rend/ITRendezvous::EnumerateDefaultDirectories, tapi3.itrendezvous_enumeratedefaultdirectories
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
 - ITRendezvous.EnumerateDefaultDirectories
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITRendezvous::EnumerateDefaultDirectories


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>EnumerateDefaultDirectories</b> method enumerates all configured default directories. This method is similar to 
<a href="https://msdn.microsoft.com/3db02f17-6fb5-467b-91f6-dc501b5472cf">get_DefaultDirectories</a> but is designed for C/C++.


## -parameters




### -param ppEnumDirectory [out]

Pointer to receive 
<a href="https://msdn.microsoft.com/9c1e83c5-c718-4a3b-916d-e844a8377a29">IEnumDirectory</a> enumerator listing default directories.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is invalid.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/9c1e83c5-c718-4a3b-916d-e844a8377a29">IEnumDirectory</a> interface returned by <b>ITRendezvous::EnumerateDefaultDirectories</b>. The application must call <b>Release</b> on the 
<b>IEnumDirectory</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/9c1e83c5-c718-4a3b-916d-e844a8377a29">IEnumDirectory</a>



<a href="https://msdn.microsoft.com/ea8b0a66-b968-4a24-95db-e702d49a2870">ITRendezvous</a>
 

 

