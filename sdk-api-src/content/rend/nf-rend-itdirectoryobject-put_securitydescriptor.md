---
UID: NF:rend.ITDirectoryObject.put_SecurityDescriptor
title: ITDirectoryObject::put_SecurityDescriptor
author: windows-sdk-content
description: The put_SecurityDescriptor method sets an IDispatch pointer on a directory service security descriptor object describing current security permissions.
old-location: tapi3\itdirectoryobject_put_securitydescriptor.htm
old-project: Tapi
ms.assetid: 1a6fe823-c794-4b6c-af51-ef03efe62606
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITDirectoryObject interface [TAPI 2.2],put_SecurityDescriptor method, ITDirectoryObject.put_SecurityDescriptor, ITDirectoryObject::put_SecurityDescriptor, _tapi3_itdirectoryobject_put_securitydescriptor, put_SecurityDescriptor, put_SecurityDescriptor method [TAPI 2.2], put_SecurityDescriptor method [TAPI 2.2],ITDirectoryObject interface, rend/ITDirectoryObject::put_SecurityDescriptor, tapi3.itdirectoryobject_put_securitydescriptor
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
-	ITDirectoryObject.put_SecurityDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITDirectoryObject::put_SecurityDescriptor


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>put_SecurityDescriptor</b> method sets an <b>IDispatch</b> pointer on a directory service security descriptor object describing current security permissions. For additional information on security descriptors, please search the Platform Software Development Kit (SDK) under "IADsSecurityDescriptor".


## -parameters




### -param pSecDes [in]

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
The <i>pSecDes</i> parameter is not a valid pointer.

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
 




## -remarks



Changes made will not take effect on the server until the 
<a href="https://msdn.microsoft.com/be53c186-c23c-4ff6-8060-f06555ab4548">ITDirectory::ModifyDirectoryObject</a> method is called.




## -see-also




<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a>



<a href="https://msdn.microsoft.com/746367e1-4319-4903-843f-7a25d60f4223">ITDirectoryObject::get_SecurityDescriptor</a>
 

 

