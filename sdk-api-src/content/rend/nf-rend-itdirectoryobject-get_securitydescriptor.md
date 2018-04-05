---
UID: NF:rend.ITDirectoryObject.get_SecurityDescriptor
title: ITDirectoryObject::get_SecurityDescriptor method
author: windows-driver-content
description: The get_SecurityDescriptor method gets an IDispatch pointer on a directory service security descriptor object describing current security permissions.
old-location: tapi3\itdirectoryobject_get_securitydescriptor.htm
old-project: Tapi
ms.assetid: 746367e1-4319-4903-843f-7a25d60f4223
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ITDirectoryObject, ITDirectoryObject interface [TAPI 2.2], get_SecurityDescriptor method, ITDirectoryObject::get_SecurityDescriptor, _tapi3_itdirectoryobject_get_securitydescriptor, get_SecurityDescriptor method [TAPI 2.2], get_SecurityDescriptor method [TAPI 2.2], ITDirectoryObject interface, get_SecurityDescriptor,ITDirectoryObject.get_SecurityDescriptor, rend/ITDirectoryObject::get_SecurityDescriptor, tapi3.itdirectoryobject_get_securitydescriptor
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
-	ITDirectoryObject.get_SecurityDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ITDirectoryObject::get_SecurityDescriptor method


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_SecurityDescriptor</b> method gets an <b>IDispatch</b> pointer on a directory service security descriptor object describing current security permissions. For additional information on security descriptors, please search the Platform Software Development Kit (SDK) under "IADsSecurityDescriptor".


## -parameters




### -param ppSecDes [out]

<b>IDispatch</b> pointer on a directory service security descriptor object.


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
The <i>ppSecDes</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Initialization of security descriptor failed.

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
</table>
 




## -remarks



If the security descriptor has not been set, this method will set <i>ppSecDes</i> to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a>



<a href="https://msdn.microsoft.com/1a6fe823-c794-4b6c-af51-ef03efe62606">ITDirectoryObject::put_SecurityDescriptor</a>
 

 

