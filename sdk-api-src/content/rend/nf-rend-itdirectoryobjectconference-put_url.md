---
UID: NF:rend.ITDirectoryObjectConference.put_Url
title: ITDirectoryObjectConference::put_Url (rend.h)
description: The put_Url method sets a URL.
helpviewer_keywords: ["ITDirectoryObjectConference interface [TAPI 2.2]","put_Url method","ITDirectoryObjectConference.put_Url","ITDirectoryObjectConference::put_Url","_tapi3_itdirectoryobjectconference_put_url","put_Url","put_Url method [TAPI 2.2]","put_Url method [TAPI 2.2]","ITDirectoryObjectConference interface","rend/ITDirectoryObjectConference::put_Url","tapi3.itdirectoryobjectconference_put_url"]
old-location: tapi3\itdirectoryobjectconference_put_url.htm
tech.root: tapi3
ms.assetid: ca275c06-fd8f-4044-b528-cc197e4f1177
ms.date: 12/05/2018
ms.keywords: ITDirectoryObjectConference interface [TAPI 2.2],put_Url method, ITDirectoryObjectConference.put_Url, ITDirectoryObjectConference::put_Url, _tapi3_itdirectoryobjectconference_put_url, put_Url, put_Url method [TAPI 2.2], put_Url method [TAPI 2.2],ITDirectoryObjectConference interface, rend/ITDirectoryObjectConference::put_Url, tapi3.itdirectoryobjectconference_put_url
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
 - ITDirectoryObjectConference::put_Url
 - rend/ITDirectoryObjectConference::put_Url
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
 - ITDirectoryObjectConference.put_Url
---

# ITDirectoryObjectConference::put_Url


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>put_Url</b> method sets a URL.

## -parameters

### -param pUrl [in]

Pointer to a <b>BSTR</b> containing the URL.

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
The <i>pUrl</i> parameter is not a valid pointer.

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
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pUrl</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobjectconference">ITDirectoryObjectConference</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-get_url">ITDirectoryObjectConference::get_Url</a>