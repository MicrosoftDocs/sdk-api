---
UID: NF:rend.ITDirectory.get_DefaultObjectTTL
title: ITDirectory::get_DefaultObjectTTL
author: windows-sdk-content
description: The get_DefaultObjectTTL method gets the default time to live (TTL) value, in seconds, for objects created. Only applies to dynamic servers.
old-location: tapi3\itdirectory_get_defaultobjectttl.htm
old-project: Tapi
ms.assetid: f0a24ad9-0020-4f62-a0f2-071b9d251f79
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITDirectory interface [TAPI 2.2],get_DefaultObjectTTL method, ITDirectory.get_DefaultObjectTTL, ITDirectory::get_DefaultObjectTTL, _tapi3_itdirectory_get_defaultobjectttl, get_DefaultObjectTTL, get_DefaultObjectTTL method [TAPI 2.2], get_DefaultObjectTTL method [TAPI 2.2],ITDirectory interface, rend/ITDirectory::get_DefaultObjectTTL, tapi3.itdirectory_get_defaultobjectttl
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
-	ITDirectory.get_DefaultObjectTTL
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITDirectory::get_DefaultObjectTTL


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_DefaultObjectTTL</b> method gets the default 
<a href="../tapi2/t_tapgloss.htm">time to live</a> (TTL) value, in seconds, for objects created. Only applies to dynamic servers.


## -parameters




### -param pTTL [out]

Pointer to TTL value, in seconds.


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
The <i>pTTL</i> parameter is not a valid pointer.

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
 




## -see-also




<a href="https://msdn.microsoft.com/9ec8c0ed-2fed-4701-acb5-86b69c10f18c">ITDirectory</a>



<a href="https://msdn.microsoft.com/aecadd26-648e-43ce-8331-ef4af24567ed">ITDirectory::put_DefaultObjectTTL</a>
 

 

