---
UID: NF:rend.ITDirectory.get_DirectoryObjects
title: ITDirectory::get_DirectoryObjects (rend.h)
description: The get_DirectoryObjects method gets the collection of objects in a given directory that matches certain criteria. This method performs the same function as EnumerateDirectoryObjects but is used by Visual Basic and other scripting languages.
helpviewer_keywords: ["ITDirectory interface [TAPI 2.2]","get_DirectoryObjects method","ITDirectory.get_DirectoryObjects","ITDirectory::get_DirectoryObjects","_tapi3_itdirectory_get_directoryobjects","get_DirectoryObjects","get_DirectoryObjects method [TAPI 2.2]","get_DirectoryObjects method [TAPI 2.2]","ITDirectory interface","rend/ITDirectory::get_DirectoryObjects","tapi3.itdirectory_get_directoryobjects"]
old-location: tapi3\itdirectory_get_directoryobjects.htm
tech.root: tapi3
ms.assetid: dd768103-4dfc-4be2-accf-38e33959102d
ms.date: 12/05/2018
ms.keywords: ITDirectory interface [TAPI 2.2],get_DirectoryObjects method, ITDirectory.get_DirectoryObjects, ITDirectory::get_DirectoryObjects, _tapi3_itdirectory_get_directoryobjects, get_DirectoryObjects, get_DirectoryObjects method [TAPI 2.2], get_DirectoryObjects method [TAPI 2.2],ITDirectory interface, rend/ITDirectory::get_DirectoryObjects, tapi3.itdirectory_get_directoryobjects
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
 - ITDirectory::get_DirectoryObjects
 - rend/ITDirectory::get_DirectoryObjects
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
 - ITDirectory.get_DirectoryObjects
---

# ITDirectory::get_DirectoryObjects


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_DirectoryObjects</b> method gets the collection of objects in a given directory that matches certain criteria. This method performs the same function as 
<a href="/windows/desktop/api/rend/nf-rend-itdirectory-enumeratedirectoryobjects">EnumerateDirectoryObjects</a> but is used by Visual Basic and other scripting languages.

## -parameters

### -param DirectoryObjectType [in]

The 
<a href="/windows/desktop/api/rend/ne-rend-directory_object_type">DIRECTORY_OBJECT_TYPE</a> criteria for object desired.

### -param pName [in]

Pointer to a <b>BSTR</b> containing the full or partial name of the object. The "*" wildcard is supported.

### -param pVariant [out]

Pointer to a <b>VARIANT</b> that receives an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a> objects in the server that match the description.

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
<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a> interface returned by <b>ITDirectory::get_DirectoryObjects</b>. The application must call <b>Release</b> on the 
<b>ITDirectoryObject</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/rend/ne-rend-directory_object_type">DIRECTORY_OBJECT_TYPE</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>



<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a>