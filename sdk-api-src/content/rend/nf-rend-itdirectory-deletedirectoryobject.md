---
UID: NF:rend.ITDirectory.DeleteDirectoryObject
title: ITDirectory::DeleteDirectoryObject
author: windows-sdk-content
description: The DeleteDirectoryObject method deletes an object from the server.
old-location: tapi3\itdirectory_deletedirectoryobject.htm
old-project: tapi
ms.assetid: 1d2bb052-6986-4407-8a37-3a74920bf78e
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: DeleteDirectoryObject, DeleteDirectoryObject method [TAPI 2.2], DeleteDirectoryObject method [TAPI 2.2],ITDirectory interface, ITDirectory interface [TAPI 2.2],DeleteDirectoryObject method, ITDirectory.DeleteDirectoryObject, ITDirectory::DeleteDirectoryObject, _tapi3_itdirectory_deletedirectoryobject, rend/ITDirectory::DeleteDirectoryObject, tapi3.itdirectory_deletedirectoryobject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rend.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITDirectory.DeleteDirectoryObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: ADAM
---

# ITDirectory::DeleteDirectoryObject


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>DeleteDirectoryObject</b> method deletes an object from the server.


## -parameters




### -param pDirectoryObject [in]

Pointer to 
<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a> that will be deleted from the directory.


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
The <i>pDirectoryObject</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RND_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The 
<a href="https://msdn.microsoft.com/b781008b-430a-444e-a700-8cde09e721b4">ITDirectory::Connect</a> method has not been invoked or did not succeed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented.

</td>
</tr>
</table>
 




## -remarks



This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.




## -see-also




<a href="https://msdn.microsoft.com/9ec8c0ed-2fed-4701-acb5-86b69c10f18c">ITDirectory</a>
 

 

