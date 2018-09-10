---
UID: NF:rend.ITRendezvous.CreateDirectoryObject
title: ITRendezvous::CreateDirectoryObject
author: windows-sdk-content
description: The CreateDirectoryObject method creates a new ITDirectoryObject object.
old-location: tapi3\itrendezvous_createdirectoryobject.htm
tech.root: tapi
ms.assetid: e3ad77cf-9112-4561-896c-2eba7e07eb19
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: CreateDirectoryObject, CreateDirectoryObject method [TAPI 2.2], CreateDirectoryObject method [TAPI 2.2],ITRendezvous interface, ITRendezvous interface [TAPI 2.2],CreateDirectoryObject method, ITRendezvous.CreateDirectoryObject, ITRendezvous::CreateDirectoryObject, _tapi3_itrendezvous_createdirectoryobject, rend/ITRendezvous::CreateDirectoryObject, tapi3.itrendezvous_createdirectoryobject
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
 - ITRendezvous.CreateDirectoryObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITRendezvous::CreateDirectoryObject


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>CreateDirectoryObject</b> method creates a new 
<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a> object.


## -parameters




### -param DirectoryObjectType [in]

The type of the object. See 
<a href="https://msdn.microsoft.com/17deac23-a81f-4bb3-a6e5-4105c504c0b5">DIRECTORY_OBJECT_TYPE</a>.


### -param pName [in]

Pointer to a <b>BSTR</b> containing the name of the object.


### -param ppDirectoryObject [out]

Pointer to receive the interface pointer for the newly created 
<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a> object.


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
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for the <i>pName</i> parameter and use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variable is no longer needed.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a> interface returned by <b>ITRendezvous::CreateDirectoryObject</b>. The application must call <b>Release</b> on the 
<b>ITDirectoryObject</b> interface to free resources associated with it.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.




## -see-also




<a href="https://msdn.microsoft.com/17deac23-a81f-4bb3-a6e5-4105c504c0b5">DIRECTORY_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a>



<a href="https://msdn.microsoft.com/ea8b0a66-b968-4a24-95db-e702d49a2870">ITRendezvous</a>
 

 

