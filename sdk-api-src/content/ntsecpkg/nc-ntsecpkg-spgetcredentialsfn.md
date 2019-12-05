---
UID: NC:ntsecpkg.SpGetCredentialsFn
title: SpGetCredentialsFn (ntsecpkg.h)
description: Retrieves the primary and supplemental credentials from the user object.
old-location: security\spgetcredentials.htm
tech.root: SecAuthN
ms.assetid: bdf96b19-30eb-4cb2-b3ec-bd6f406233c5
ms.date: 12/05/2018
ms.keywords: SpGetCredentials, SpGetCredentials callback function [Security], SpGetCredentialsFn, SpGetCredentialsFn callback, _ssp_spgetcredentials, ntsecpkg/SpGetCredentials, security.spgetcredentials
ms.topic: callback
f1_keywords:
- ntsecpkg/SpGetCredentials
dev_langs:
- c++
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Ntsecpkg.h
api_name:
- SpGetCredentials
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SpGetCredentialsFn callback function


## -description


The <b>SpGetCredentials</b> function retrieves the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">primary</a> and <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">supplemental credentials</a> from the user object.


## -parameters




### -param CredentialHandle [in]

A handle to the credentials to be retrieved.


### -param Credentials [out]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure that receives the credentials.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code indicating the reason it failed. The following  lists common reasons for failure and the error codes that the function should return. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INSUFFICIENT_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not sufficient memory to retrieve the credentials.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
</table>
 




## -remarks



SSP/APs must implement the <b>SpGetCredentials</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpGetCredentials</b> function is available in the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>
 

 

