---
UID: NF:rend.ITDirectoryObjectConference.put_Originator
title: ITDirectoryObjectConference::put_Originator (rend.h)
description: The put_Originator method sets the originator's user name.
helpviewer_keywords: ["ITDirectoryObjectConference interface [TAPI 2.2]","put_Originator method","ITDirectoryObjectConference.put_Originator","ITDirectoryObjectConference::put_Originator","_tapi3_itdirectoryobjectconference_put_originator","put_Originator","put_Originator method [TAPI 2.2]","put_Originator method [TAPI 2.2]","ITDirectoryObjectConference interface","rend/ITDirectoryObjectConference::put_Originator","tapi3.itdirectoryobjectconference_put_originator"]
old-location: tapi3\itdirectoryobjectconference_put_originator.htm
tech.root: tapi3
ms.assetid: 97e8b966-b65c-4c19-ac61-0b952657aec1
ms.date: 12/05/2018
ms.keywords: ITDirectoryObjectConference interface [TAPI 2.2],put_Originator method, ITDirectoryObjectConference.put_Originator, ITDirectoryObjectConference::put_Originator, _tapi3_itdirectoryobjectconference_put_originator, put_Originator, put_Originator method [TAPI 2.2], put_Originator method [TAPI 2.2],ITDirectoryObjectConference interface, rend/ITDirectoryObjectConference::put_Originator, tapi3.itdirectoryobjectconference_put_originator
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
 - ITDirectoryObjectConference::put_Originator
 - rend/ITDirectoryObjectConference::put_Originator
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
 - ITDirectoryObjectConference.put_Originator
---

# ITDirectoryObjectConference::put_Originator


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>put_Originator</b> method sets the originator's user name.

## -parameters

### -param pOriginator [in]

Pointer to a <b>BSTR</b> containing the originator's user name.

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
The <i>pOriginator</i> parameter is not a valid pointer.

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
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pOriginator</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

The originator's name, along with the machine name set in 
<a href="/windows/desktop/Tapi/itsdp-put-machineaddress">put_MachineAddress</a>, are collectively the originator of the conference, and both are in the o= line of the SDP.

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobjectconference">ITDirectoryObjectConference</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-get_originator">ITDirectoryObjectConference::get_Originator</a>