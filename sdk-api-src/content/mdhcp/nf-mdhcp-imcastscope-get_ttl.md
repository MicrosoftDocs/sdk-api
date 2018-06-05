---
UID: NF:mdhcp.IMcastScope.get_TTL
title: IMcastScope::get_TTL
author: windows-sdk-content
description: The get_TTL method obtains the time to live value for the multicast scope.
old-location: tapi3\imcastscope_get_ttl.htm
old-project: Tapi
ms.assetid: 68e402e5-87ae-49fd-9149-8eb79a0a8aee
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IMcastScope interface [TAPI 2.2],get_TTL method, IMcastScope.get_TTL, IMcastScope::get_TTL, _tapi3_imcastscope_get_ttl, get_TTL, get_TTL method [TAPI 2.2], get_TTL method [TAPI 2.2],IMcastScope interface, mdhcp/IMcastScope::get_TTL, tapi3.imcastscope_get_ttl
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mdhcp.dll
api_name:
-	IMcastScope.get_TTL
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Mdhcp.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMcastScope::get_TTL


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_TTL</b> method obtains the time to live value for the multicast scope.


## -parameters




### -param pTTL [out]

Pointer to a time to live value for multicast scope.


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
 

 

