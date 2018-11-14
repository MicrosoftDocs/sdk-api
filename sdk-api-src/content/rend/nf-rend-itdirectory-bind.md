---
UID: NF:rend.ITDirectory.Bind
title: ITDirectory::Bind
author: windows-sdk-content
description: The Bind method binds to the server.
old-location: tapi3\itdirectory_bind.htm
tech.root: tapi
ms.assetid: 4bcf994c-3091-445e-ad79-91958e48960a
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Bind, Bind method [TAPI 2.2], Bind method [TAPI 2.2],ITDirectory interface, ITDirectory interface [TAPI 2.2],Bind method, ITDirectory.Bind, ITDirectory::Bind, _tapi3_itdirectory_bind, rend/ITDirectory::Bind, tapi3.itdirectory_bind
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ITDirectory.Bind
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- rend.h
: 
- ITDirectory.Bind
: 
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


<a href="https://msdn.microsoft.com/27bcf36a-1826-4603-9821-22fcc5c1e186">RENDBIND</a> flags indicator of whether all parameters must be validated or can take a default.


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
<a href="https://msdn.microsoft.com/b781008b-430a-444e-a700-8cde09e721b4">ITDirectory::Connect</a> method has not been invoked or did not succeed.

</td>
</tr>
</table>
 




## -remarks



The input variables <i>pDomainName</i>, <i>pUserName</i>, and <i>pPassword</i> can be <b>NULL</b>.

Calling this function is optional. However, some directory operations require the user to be authenticated first. It is always safe to call 
<b>Bind</b>.

The application must use 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for the <i>pDomainName</i>, <i>pUserName</i>, and <i>pPassword</i> parameters. The application must use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variables are no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/9ec8c0ed-2fed-4701-acb5-86b69c10f18c">ITDirectory</a>
 

 

