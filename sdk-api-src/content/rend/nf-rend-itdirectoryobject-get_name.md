---
UID: NF:rend.ITDirectoryObject.get_Name
title: ITDirectoryObject::get_Name (rend.h)
description: The get_Name method gets the name of the directory object.
helpviewer_keywords: ["ITDirectoryObject interface [TAPI 2.2]","get_Name method","ITDirectoryObject.get_Name","ITDirectoryObject::get_Name","_tapi3_itdirectoryobject_get_name","get_Name","get_Name method [TAPI 2.2]","get_Name method [TAPI 2.2]","ITDirectoryObject interface","rend/ITDirectoryObject::get_Name","tapi3.itdirectoryobject_get_name"]
old-location: tapi3\itdirectoryobject_get_name.htm
tech.root: tapi3
ms.assetid: b24c1e69-5ba1-4597-86fb-2233707a1acf
ms.date: 12/05/2018
ms.keywords: ITDirectoryObject interface [TAPI 2.2],get_Name method, ITDirectoryObject.get_Name, ITDirectoryObject::get_Name, _tapi3_itdirectoryobject_get_name, get_Name, get_Name method [TAPI 2.2], get_Name method [TAPI 2.2],ITDirectoryObject interface, rend/ITDirectoryObject::get_Name, tapi3.itdirectoryobject_get_name
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
 - ITDirectoryObject::get_Name
 - rend/ITDirectoryObject::get_Name
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
 - ITDirectoryObject.get_Name
---

# ITDirectoryObject::get_Name


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_Name</b> method gets the name of the directory object.

## -parameters

### -param ppName [out]

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
Invalid pointer.

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

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppName</i> parameter.

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectoryobject-put_name">ITDirectoryObject::put_Name</a>