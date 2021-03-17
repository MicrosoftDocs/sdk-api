---
UID: NF:rend.ITDirectory.ModifyDirectoryObject
title: ITDirectory::ModifyDirectoryObject (rend.h)
description: The ModifyDirectoryObject method commits directory modifications to the server.
helpviewer_keywords: ["ITDirectory interface [TAPI 2.2]","ModifyDirectoryObject method","ITDirectory.ModifyDirectoryObject","ITDirectory::ModifyDirectoryObject","ModifyDirectoryObject","ModifyDirectoryObject method [TAPI 2.2]","ModifyDirectoryObject method [TAPI 2.2]","ITDirectory interface","_tapi3_itdirectory_modifydirectoryobject","rend/ITDirectory::ModifyDirectoryObject","tapi3.itdirectory_modifydirectoryobject"]
old-location: tapi3\itdirectory_modifydirectoryobject.htm
tech.root: tapi3
ms.assetid: be53c186-c23c-4ff6-8060-f06555ab4548
ms.date: 12/05/2018
ms.keywords: ITDirectory interface [TAPI 2.2],ModifyDirectoryObject method, ITDirectory.ModifyDirectoryObject, ITDirectory::ModifyDirectoryObject, ModifyDirectoryObject, ModifyDirectoryObject method [TAPI 2.2], ModifyDirectoryObject method [TAPI 2.2],ITDirectory interface, _tapi3_itdirectory_modifydirectoryobject, rend/ITDirectory::ModifyDirectoryObject, tapi3.itdirectory_modifydirectoryobject
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
 - ITDirectory::ModifyDirectoryObject
 - rend/ITDirectory::ModifyDirectoryObject
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
 - ITDirectory.ModifyDirectoryObject
---

# ITDirectory::ModifyDirectoryObject


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ModifyDirectoryObject</b> method commits directory modifications to the server.

## -parameters

### -param pDirectoryObject [in]

Pointer to 
<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a> modified.

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

Changes made to 
<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a> will not take effect on the server until this method is called.

Some attributes cannot be modified, and an attempt to modify them will fail. For an example, see the Remarks section of 
<a href="/windows/desktop/api/rend/nf-rend-itdirectoryobjectuser-put_ipphoneprimary">ITDirectoryObjectUser::put_IPPhonePrimary</a>.

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>