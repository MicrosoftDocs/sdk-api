---
UID: NF:rend.ITDirectoryObjectConference.put_Description
title: ITDirectoryObjectConference::put_Description (rend.h)
description: The put_Description method sets the description of the conference.helpviewer_keywords: ["ITDirectoryObjectConference interface [TAPI 2.2]","put_Description method","ITDirectoryObjectConference.put_Description","ITDirectoryObjectConference::put_Description","_tapi3_itdirectoryobjectconference_put_description","put_Description","put_Description method [TAPI 2.2]","put_Description method [TAPI 2.2]","ITDirectoryObjectConference interface","rend/ITDirectoryObjectConference::put_Description","tapi3.itdirectoryobjectconference_put_description"]
old-location: tapi3\itdirectoryobjectconference_put_description.htm
tech.root: Tapi
ms.assetid: 46f58067-22ec-490e-b6cc-0fdc12dbb8f7
ms.date: 12/05/2018
ms.keywords: ITDirectoryObjectConference interface [TAPI 2.2],put_Description method, ITDirectoryObjectConference.put_Description, ITDirectoryObjectConference::put_Description, _tapi3_itdirectoryobjectconference_put_description, put_Description, put_Description method [TAPI 2.2], put_Description method [TAPI 2.2],ITDirectoryObjectConference interface, rend/ITDirectoryObjectConference::put_Description, tapi3.itdirectoryobjectconference_put_description
f1_keywords:
- rend/ITDirectoryObjectConference.put_Description
dev_langs:
- c++
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
- ITDirectoryObjectConference.put_Description
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITDirectoryObjectConference::put_Description


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>put_Description</b> method sets the description of the conference.


## -parameters




### -param pDescription [in]

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
The <i>pDescription</i> parameter is not a valid pointer.

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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pDescription</i> parameter and use 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rend/nn-rend-itdirectoryobjectconference">ITDirectoryObjectConference</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-get_description">ITDirectoryObjectConference::get_Description</a>
 

 

