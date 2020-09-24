---
UID: NF:rend.ITDirectoryObject.get_SecurityDescriptor
title: ITDirectoryObject::get_SecurityDescriptor (rend.h)
description: The get_SecurityDescriptor method gets an IDispatch pointer on a directory service security descriptor object describing current security permissions.
helpviewer_keywords: ["ITDirectoryObject interface [TAPI 2.2]","get_SecurityDescriptor method","ITDirectoryObject.get_SecurityDescriptor","ITDirectoryObject::get_SecurityDescriptor","_tapi3_itdirectoryobject_get_securitydescriptor","get_SecurityDescriptor","get_SecurityDescriptor method [TAPI 2.2]","get_SecurityDescriptor method [TAPI 2.2]","ITDirectoryObject interface","rend/ITDirectoryObject::get_SecurityDescriptor","tapi3.itdirectoryobject_get_securitydescriptor"]
old-location: tapi3\itdirectoryobject_get_securitydescriptor.htm
tech.root: tapi3
ms.assetid: 746367e1-4319-4903-843f-7a25d60f4223
ms.date: 12/05/2018
ms.keywords: ITDirectoryObject interface [TAPI 2.2],get_SecurityDescriptor method, ITDirectoryObject.get_SecurityDescriptor, ITDirectoryObject::get_SecurityDescriptor, _tapi3_itdirectoryobject_get_securitydescriptor, get_SecurityDescriptor, get_SecurityDescriptor method [TAPI 2.2], get_SecurityDescriptor method [TAPI 2.2],ITDirectoryObject interface, rend/ITDirectoryObject::get_SecurityDescriptor, tapi3.itdirectoryobject_get_securitydescriptor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITDirectoryObject::get_SecurityDescriptor
 - rend/ITDirectoryObject::get_SecurityDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITDirectoryObject.get_SecurityDescriptor
---

# ITDirectoryObject::get_SecurityDescriptor


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
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

<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectoryobject-put_securitydescriptor">ITDirectoryObject::put_SecurityDescriptor</a>