---
UID: NF:rend.ITRendezvous.CreateDirectoryObject
title: ITRendezvous::CreateDirectoryObject (rend.h)
description: The CreateDirectoryObject method creates a new ITDirectoryObject object.
helpviewer_keywords: ["CreateDirectoryObject","CreateDirectoryObject method [TAPI 2.2]","CreateDirectoryObject method [TAPI 2.2]","ITRendezvous interface","ITRendezvous interface [TAPI 2.2]","CreateDirectoryObject method","ITRendezvous.CreateDirectoryObject","ITRendezvous::CreateDirectoryObject","_tapi3_itrendezvous_createdirectoryobject","rend/ITRendezvous::CreateDirectoryObject","tapi3.itrendezvous_createdirectoryobject"]
old-location: tapi3\itrendezvous_createdirectoryobject.htm
tech.root: tapi3
ms.assetid: e3ad77cf-9112-4561-896c-2eba7e07eb19
ms.date: 12/05/2018
ms.keywords: CreateDirectoryObject, CreateDirectoryObject method [TAPI 2.2], CreateDirectoryObject method [TAPI 2.2],ITRendezvous interface, ITRendezvous interface [TAPI 2.2],CreateDirectoryObject method, ITRendezvous.CreateDirectoryObject, ITRendezvous::CreateDirectoryObject, _tapi3_itrendezvous_createdirectoryobject, rend/ITRendezvous::CreateDirectoryObject, tapi3.itrendezvous_createdirectoryobject
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
 - ITRendezvous::CreateDirectoryObject
 - rend/ITRendezvous::CreateDirectoryObject
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
 - ITRendezvous.CreateDirectoryObject
---

# ITRendezvous::CreateDirectoryObject


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>CreateDirectoryObject</b> method creates a new 
<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a> object.

## -parameters

### -param DirectoryObjectType [in]

The type of the object. See 
<a href="/windows/desktop/api/rend/ne-rend-directory_object_type">DIRECTORY_OBJECT_TYPE</a>.

### -param pName [in]

Pointer to a <b>BSTR</b> containing the name of the object.

### -param ppDirectoryObject [out]

Pointer to receive the interface pointer for the newly created 
<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a> object.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>DirectoryObjectType</i> parameter is not valid.

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

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pName</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a> interface returned by <b>ITRendezvous::CreateDirectoryObject</b>. The application must call <b>Release</b> on the 
<b>ITDirectoryObject</b> interface to free resources associated with it.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.

## -see-also

<a href="/windows/desktop/api/rend/ne-rend-directory_object_type">DIRECTORY_OBJECT_TYPE</a>



<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a>



<a href="/windows/desktop/api/rend/nn-rend-itrendezvous">ITRendezvous</a>