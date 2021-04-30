---
UID: NF:rend.ITRendezvous.CreateDirectory
title: ITRendezvous::CreateDirectory (rend.h)
description: The CreateDirectory method creates an ITDirectory object corresponding to a directory of the given type and name.
helpviewer_keywords: ["CreateDirectory","CreateDirectory method [TAPI 2.2]","CreateDirectory method [TAPI 2.2]","ITRendezvous interface","ITRendezvous interface [TAPI 2.2]","CreateDirectory method","ITRendezvous.CreateDirectory","ITRendezvous::CreateDirectory","_tapi3_itrendezvous_createdirectory","rend/ITRendezvous::CreateDirectory","tapi3.itrendezvous_createdirectory"]
old-location: tapi3\itrendezvous_createdirectory.htm
tech.root: tapi3
ms.assetid: b285f852-a017-4dcd-b32e-afb2296487a5
ms.date: 12/05/2018
ms.keywords: CreateDirectory, CreateDirectory method [TAPI 2.2], CreateDirectory method [TAPI 2.2],ITRendezvous interface, ITRendezvous interface [TAPI 2.2],CreateDirectory method, ITRendezvous.CreateDirectory, ITRendezvous::CreateDirectory, _tapi3_itrendezvous_createdirectory, rend/ITRendezvous::CreateDirectory, tapi3.itrendezvous_createdirectory
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
 - ITRendezvous::CreateDirectory
 - rend/ITRendezvous::CreateDirectory
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
 - ITRendezvous.CreateDirectory
---

# ITRendezvous::CreateDirectory


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>CreateDirectory</b> method creates an ITDirectory object corresponding to a directory of the given type and name.

## -parameters

### -param DirectoryType [in]

The type of the directory. See 
<a href="/windows/desktop/api/rend/ne-rend-directory_type">DIRECTORY_TYPE</a>.

### -param pName [in]

Pointer to a <b>BSTR</b> containing the name of the directory to be created.

### -param ppDir [out]

Pointer to receive an 
<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a> object of the type specified above.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pName</i> or <i>ppDir</i> parameter is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>DirectoryType</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

For directories of type DT_NTDS, <i>pName</i> is ignored because Rendezvous supports using only the local domain controller (DC).

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pName</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a> interface returned by <b>ITRendezvous::CreateDirectory</b>. The application must call <b>Release</b> on the 
<b>ITDirectory</b> interface to free resources associated with it.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.

## -see-also

<a href="/windows/desktop/api/rend/ne-rend-directory_type">DIRECTORY_TYPE</a>



<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>



<a href="/windows/desktop/api/rend/nn-rend-itrendezvous">ITRendezvous</a>