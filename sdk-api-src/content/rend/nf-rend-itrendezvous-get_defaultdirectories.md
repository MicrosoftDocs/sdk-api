---
UID: NF:rend.ITRendezvous.get_DefaultDirectories
title: ITRendezvous::get_DefaultDirectories (rend.h)
author: windows-sdk-content
description: The get_DefaultDirectories method enumerates all configured default directories. This method is similar to EnumerateDefaultDirectories but is provided for use by Visual Basic and other scripting languages.
old-location: tapi3\itrendezvous_get_defaultdirectories.htm
tech.root: Tapi
ms.assetid: 3db02f17-6fb5-467b-91f6-dc501b5472cf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITRendezvous interface [TAPI 2.2],get_DefaultDirectories method, ITRendezvous.get_DefaultDirectories, ITRendezvous::get_DefaultDirectories, _tapi3_itrendezvous_get_defaultdirectories, get_DefaultDirectories, get_DefaultDirectories method [TAPI 2.2], get_DefaultDirectories method [TAPI 2.2],ITRendezvous interface, rend/ITRendezvous::get_DefaultDirectories, tapi3.itrendezvous_get_defaultdirectories
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
 - ITRendezvous.get_DefaultDirectories
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITRendezvous::get_DefaultDirectories


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_DefaultDirectories</b> method enumerates all configured default directories. This method is similar to 
<a href="https://msdn.microsoft.com/fe89a370-32ed-4519-bb98-9d9ea7615eb7">EnumerateDefaultDirectories</a> but is provided for use by Visual Basic and other scripting languages.


## -parameters




### -param pVariant [out]

Pointer to a <b>VARIANT</b> that will receive an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/9ec8c0ed-2fed-4701-acb5-86b69c10f18c">ITDirectory</a> interface pointers.


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
Insufficient memory exists to create a collection.

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
<a href="https://msdn.microsoft.com/9ec8c0ed-2fed-4701-acb5-86b69c10f18c">ITDirectory</a> interface returned by <b>ITRendezvous::get_DefaultDirectories</b>. The application must call <b>Release</b> on the 
<b>ITDirectory</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>



<a href="https://msdn.microsoft.com/9ec8c0ed-2fed-4701-acb5-86b69c10f18c">ITDirectory</a>



<a href="https://msdn.microsoft.com/ea8b0a66-b968-4a24-95db-e702d49a2870">ITRendezvous</a>
 

 

