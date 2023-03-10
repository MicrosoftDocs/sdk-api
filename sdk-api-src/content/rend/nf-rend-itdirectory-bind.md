---
UID: NF:rend.ITDirectory.Bind
title: ITDirectory::Bind (rend.h)
description: The Bind method binds to the server.
helpviewer_keywords: ["Bind","Bind method [TAPI 2.2]","Bind method [TAPI 2.2]","ITDirectory interface","ITDirectory interface [TAPI 2.2]","Bind method","ITDirectory.Bind","ITDirectory::Bind","_tapi3_itdirectory_bind","rend/ITDirectory::Bind","tapi3.itdirectory_bind"]
old-location: tapi3\itdirectory_bind.htm
tech.root: tapi3
ms.assetid: 4bcf994c-3091-445e-ad79-91958e48960a
ms.date: 12/05/2018
ms.keywords: Bind, Bind method [TAPI 2.2], Bind method [TAPI 2.2],ITDirectory interface, ITDirectory interface [TAPI 2.2],Bind method, ITDirectory.Bind, ITDirectory::Bind, _tapi3_itdirectory_bind, rend/ITDirectory::Bind, tapi3.itdirectory_bind
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
 - ITDirectory::Bind
 - rend/ITDirectory::Bind
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
 - ITDirectory.Bind
---

# ITDirectory::Bind


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>Bind</b> method binds to the server.

## -parameters

### -param pDomainName [in]

Pointer to a <b>BSTR</b> containing the user's domain name.

### -param pUserName [in]

Pointer to a <b>BSTR</b> containing the user's name.

### -param pPassword [in]

Pointer to a <b>BSTR</b> containing the user's password.

### -param lFlags [in]

<a href="/windows/desktop/Tapi/rendbind--constants">RENDBIND</a> flags indicator of whether all parameters must be validated or can take a default.

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
The <i>pDomainName</i>, <i>pUserName</i>, or <i>pPassword</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A password is required but was not supplied, the domain and user are not supplied, or the domain was supplied but the user was not.

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
</table>

## -remarks

The input variables <i>pDomainName</i>, <i>pUserName</i>, and <i>pPassword</i> can be <b>NULL</b>.

Calling this function is optional. However, some directory operations require the user to be authenticated first. It is always safe to call 
<b>Bind</b>.

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pDomainName</i>, <i>pUserName</i>, and <i>pPassword</i> parameters. The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variables are no longer needed.

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>