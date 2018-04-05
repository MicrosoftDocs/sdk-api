---
UID: NF:rend.ITDirectoryObject.EnumerateDialableAddrs
title: ITDirectoryObject::EnumerateDialableAddrs method
author: windows-driver-content
description: The EnumerateDialableAddrs method creates an enumerator of all dialable addresses of a given type from the directory.
old-location: tapi3\itdirectoryobject_enumeratedialableaddrs.htm
old-project: Tapi
ms.assetid: cee7a00e-e601-47bf-b64b-61085511da97
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: EnumerateDialableAddrs method [TAPI 2.2], EnumerateDialableAddrs method [TAPI 2.2], ITDirectoryObject interface, EnumerateDialableAddrs,ITDirectoryObject.EnumerateDialableAddrs, ITDirectoryObject, ITDirectoryObject interface [TAPI 2.2], EnumerateDialableAddrs method, ITDirectoryObject::EnumerateDialableAddrs, _tapi3_itdirectoryobject_enumeratedialableaddrs, rend/ITDirectoryObject::EnumerateDialableAddrs, tapi3.itdirectoryobject_enumeratedialableaddrs
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
req.typenames: RND_ADVERTISING_SCOPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Rend.dll
api_name:
-	ITDirectoryObject.EnumerateDialableAddrs
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ITDirectoryObject::EnumerateDialableAddrs method


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>EnumerateDialableAddrs</b> method creates an enumerator of all dialable addresses of a given type from the directory.


## -parameters




### -param dwAddressType [in]

Indicator of the address type.


### -param ppEnumDialableAddrs [out]

Pointer to the 
<a href="https://msdn.microsoft.com/0a64cb89-9e44-4af1-9b0f-2eec6e5267c7">IEnumDialableAddrs</a> interface.


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
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR</b></dt>
</dl>
</td>
<td width="60%">
Method failed.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/0a64cb89-9e44-4af1-9b0f-2eec6e5267c7">IEnumDialableAddrs</a> interface returned by <b>ITDirectoryObject::EnumerateDialableAddrs</b>. The application must call <b>Release</b> on the 
<b>IEnumDialableAddrs</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/0a64cb89-9e44-4af1-9b0f-2eec6e5267c7">IEnumDialableAddrs</a>



<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a>
 

 

