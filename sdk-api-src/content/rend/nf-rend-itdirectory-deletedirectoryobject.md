---
UID: NF:rend.ITDirectory.DeleteDirectoryObject
title: ITDirectory::DeleteDirectoryObject (rend.h)
description: The DeleteDirectoryObject method deletes an object from the server.
helpviewer_keywords: ["DeleteDirectoryObject","DeleteDirectoryObject method [TAPI 2.2]","DeleteDirectoryObject method [TAPI 2.2]","ITDirectory interface","ITDirectory interface [TAPI 2.2]","DeleteDirectoryObject method","ITDirectory.DeleteDirectoryObject","ITDirectory::DeleteDirectoryObject","_tapi3_itdirectory_deletedirectoryobject","rend/ITDirectory::DeleteDirectoryObject","tapi3.itdirectory_deletedirectoryobject"]
old-location: tapi3\itdirectory_deletedirectoryobject.htm
tech.root: tapi3
ms.assetid: 1d2bb052-6986-4407-8a37-3a74920bf78e
ms.date: 12/05/2018
ms.keywords: DeleteDirectoryObject, DeleteDirectoryObject method [TAPI 2.2], DeleteDirectoryObject method [TAPI 2.2],ITDirectory interface, ITDirectory interface [TAPI 2.2],DeleteDirectoryObject method, ITDirectory.DeleteDirectoryObject, ITDirectory::DeleteDirectoryObject, _tapi3_itdirectory_deletedirectoryobject, rend/ITDirectory::DeleteDirectoryObject, tapi3.itdirectory_deletedirectoryobject
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
 - ITDirectory::DeleteDirectoryObject
 - rend/ITDirectory::DeleteDirectoryObject
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
 - ITDirectory.DeleteDirectoryObject
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
<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a> that will be deleted from the directory.

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
<a href="/windows/desktop/api/rend/nf-rend-itdirectory-connect">ITDirectory::Connect</a> method has not been invoked or did not succeed.

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

<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>