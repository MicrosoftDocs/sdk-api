---
UID: NF:rend.ITDirectory.AddDirectoryObject
title: ITDirectory::AddDirectoryObject (rend.h)
description: The AddDirectoryObject method adds an ITDirectoryObject object to the server. This may be a directory or a user machine mapping.
helpviewer_keywords: ["AddDirectoryObject","AddDirectoryObject method [TAPI 2.2]","AddDirectoryObject method [TAPI 2.2]","ITDirectory interface","ITDirectory interface [TAPI 2.2]","AddDirectoryObject method","ITDirectory.AddDirectoryObject","ITDirectory::AddDirectoryObject","_tapi3_itdirectory_adddirectoryobject","rend/ITDirectory::AddDirectoryObject","tapi3.itdirectory_adddirectoryobject"]
old-location: tapi3\itdirectory_adddirectoryobject.htm
tech.root: tapi3
ms.assetid: 7a379bdc-50e3-4034-ac16-d20d1b03cd35
ms.date: 12/05/2018
ms.keywords: AddDirectoryObject, AddDirectoryObject method [TAPI 2.2], AddDirectoryObject method [TAPI 2.2],ITDirectory interface, ITDirectory interface [TAPI 2.2],AddDirectoryObject method, ITDirectory.AddDirectoryObject, ITDirectory::AddDirectoryObject, _tapi3_itdirectory_adddirectoryobject, rend/ITDirectory::AddDirectoryObject, tapi3.itdirectory_adddirectoryobject
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
 - ITDirectory::AddDirectoryObject
 - rend/ITDirectory::AddDirectoryObject
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
 - ITDirectory.AddDirectoryObject
---

# ITDirectory::AddDirectoryObject


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>AddDirectoryObject</b> method adds an 
<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a> object to the server. This may be a directory or a user machine mapping.

## -parameters

### -param pDirectoryObject [in]

The object that will be added into the directory.

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

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>