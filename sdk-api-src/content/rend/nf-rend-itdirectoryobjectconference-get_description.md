---
UID: NF:rend.ITDirectoryObjectConference.get_Description
title: ITDirectoryObjectConference::get_Description (rend.h)
description: The get_Description method gets the description of the conference.
helpviewer_keywords: ["ITDirectoryObjectConference interface [TAPI 2.2]","get_Description method","ITDirectoryObjectConference.get_Description","ITDirectoryObjectConference::get_Description","_tapi3_itdirectoryobjectconference_get_description","get_Description","get_Description method [TAPI 2.2]","get_Description method [TAPI 2.2]","ITDirectoryObjectConference interface","rend/ITDirectoryObjectConference::get_Description","tapi3.itdirectoryobjectconference_get_description"]
old-location: tapi3\itdirectoryobjectconference_get_description.htm
tech.root: tapi3
ms.assetid: f90defa9-5e70-4168-9a07-ccb520bd5a1f
ms.date: 12/05/2018
ms.keywords: ITDirectoryObjectConference interface [TAPI 2.2],get_Description method, ITDirectoryObjectConference.get_Description, ITDirectoryObjectConference::get_Description, _tapi3_itdirectoryobjectconference_get_description, get_Description, get_Description method [TAPI 2.2], get_Description method [TAPI 2.2],ITDirectoryObjectConference interface, rend/ITDirectoryObjectConference::get_Description, tapi3.itdirectoryobjectconference_get_description
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
 - ITDirectoryObjectConference::get_Description
 - rend/ITDirectoryObjectConference::get_Description
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
 - ITDirectoryObjectConference.get_Description
---

# ITDirectoryObjectConference::get_Description


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_Description</b> method gets the description of the conference.

## -parameters

### -param ppDescription [out]

Pointer to a <b>BSTR</b> containing the description of the conference.

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
The <i>ppDescription</i> parameter is not a valid pointer.

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

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppDescription</i> parameter.

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobjectconference">ITDirectoryObjectConference</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-put_description">ITDirectoryObjectConference::put_Description</a>