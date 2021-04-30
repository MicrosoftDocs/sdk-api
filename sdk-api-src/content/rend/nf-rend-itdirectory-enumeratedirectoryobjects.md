---
UID: NF:rend.ITDirectory.EnumerateDirectoryObjects
title: ITDirectory::EnumerateDirectoryObjects (rend.h)
description: The EnumerateDirectoryObjects method creates an enumeration of directory objects of a given type and name.
helpviewer_keywords: ["EnumerateDirectoryObjects","EnumerateDirectoryObjects method [TAPI 2.2]","EnumerateDirectoryObjects method [TAPI 2.2]","ITDirectory interface","ITDirectory interface [TAPI 2.2]","EnumerateDirectoryObjects method","ITDirectory.EnumerateDirectoryObjects","ITDirectory::EnumerateDirectoryObjects","_tapi3_itdirectory_enumeratedirectoryobjects","rend/ITDirectory::EnumerateDirectoryObjects","tapi3.itdirectory_enumeratedirectoryobjects"]
old-location: tapi3\itdirectory_enumeratedirectoryobjects.htm
tech.root: tapi3
ms.assetid: 4d7e0fd5-b85b-41e0-9603-132243a9a265
ms.date: 12/05/2018
ms.keywords: EnumerateDirectoryObjects, EnumerateDirectoryObjects method [TAPI 2.2], EnumerateDirectoryObjects method [TAPI 2.2],ITDirectory interface, ITDirectory interface [TAPI 2.2],EnumerateDirectoryObjects method, ITDirectory.EnumerateDirectoryObjects, ITDirectory::EnumerateDirectoryObjects, _tapi3_itdirectory_enumeratedirectoryobjects, rend/ITDirectory::EnumerateDirectoryObjects, tapi3.itdirectory_enumeratedirectoryobjects
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
 - ITDirectory::EnumerateDirectoryObjects
 - rend/ITDirectory::EnumerateDirectoryObjects
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
 - ITDirectory.EnumerateDirectoryObjects
---

# ITDirectory::EnumerateDirectoryObjects


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>EnumerateDirectoryObjects</b> method creates an enumeration of directory objects of a given type and name.

## -parameters

### -param DirectoryObjectType [in]

The 
<a href="/windows/desktop/api/rend/ne-rend-directory_object_type">DIRECTORY_OBJECT_TYPE</a> criteria for object desired.

### -param pName [in]

Pointer to a <b>BSTR</b> containing the full or partial name of the object. The "*" wildcard is supported.

### -param ppEnumObject [out]

Pointer to receive 
<a href="/windows/desktop/api/rend/nn-rend-ienumdirectoryobject">IEnumDirectoryObject</a> interface pointer for the enumerator of matching objects.

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

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pName</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/rend/nn-rend-ienumdirectoryobject">IEnumDirectoryObject</a> interface returned by <b>ITDirectory::EnumerateDirectoryObjects</b>. The application must call <b>Release</b> on the 
<b>IEnumDirectoryObject</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/rend/ne-rend-directory_object_type">DIRECTORY_OBJECT_TYPE</a>



<a href="/windows/desktop/api/rend/nn-rend-ienumdirectoryobject">IEnumDirectoryObject</a>



<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>