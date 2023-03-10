---
UID: NF:rend.ITDirectoryObject.put_Name
title: ITDirectoryObject::put_Name (rend.h)
description: The put_Name method sets the name of the directory object.
helpviewer_keywords: ["ITDirectoryObject interface [TAPI 2.2]","put_Name method","ITDirectoryObject.put_Name","ITDirectoryObject::put_Name","_tapi3_itdirectoryobject_put_name","put_Name","put_Name method [TAPI 2.2]","put_Name method [TAPI 2.2]","ITDirectoryObject interface","rend/ITDirectoryObject::put_Name","tapi3.itdirectoryobject_put_name"]
old-location: tapi3\itdirectoryobject_put_name.htm
tech.root: tapi3
ms.assetid: 398ba207-bdd7-4090-ac8b-72badbb401e3
ms.date: 12/05/2018
ms.keywords: ITDirectoryObject interface [TAPI 2.2],put_Name method, ITDirectoryObject.put_Name, ITDirectoryObject::put_Name, _tapi3_itdirectoryobject_put_name, put_Name, put_Name method [TAPI 2.2], put_Name method [TAPI 2.2],ITDirectoryObject interface, rend/ITDirectoryObject::put_Name, tapi3.itdirectoryobject_put_name
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
 - ITDirectoryObject::put_Name
 - rend/ITDirectoryObject::put_Name
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
 - ITDirectoryObject.put_Name
---

# ITDirectoryObject::put_Name


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>put_Name</b> method sets the name of the directory object.

## -parameters

### -param pName [in]

Pointer to <b>BSTR</b> representation of directory name.

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
The <i>pName</i> parameter is not a valid pointer.

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
<a href="/windows/desktop/api/rend/nf-rend-itdirectory-modifydirectoryobject">ITDirectory::ModifyDirectoryObject</a> method is called.

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pName</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectoryobject-get_name">ITDirectoryObject::get_Name</a>