---
UID: NC:ntsecpkg.KspMakeSignatureFn
title: KspMakeSignatureFn (ntsecpkg.h)
description: Generates a signature based on the specified message and security context.
helpviewer_keywords: ["KspMakeSignatureFn","KspMakeSignatureFn callback","SpMakeSignature","SpMakeSignature callback function [Security]","_ssp_spmakesignature","ntsecpkg/SpMakeSignature","security.spmakesignature"]
old-location: security\spmakesignature.htm
tech.root: security
ms.assetid: 9db828f3-b15c-4e22-bbd8-5daa223b2be0
ms.date: 12/05/2018
ms.keywords: KspMakeSignatureFn, KspMakeSignatureFn callback, SpMakeSignature, SpMakeSignature callback function [Security], _ssp_spmakesignature, ntsecpkg/SpMakeSignature, security.spmakesignature
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - KspMakeSignatureFn
 - ntsecpkg/KspMakeSignatureFn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - SpMakeSignature
---

# KspMakeSignatureFn callback function


## -description

The <b>SpMakeSignature</b> function generates a <a href="/windows/desktop/SecGloss/d-gly">signature</a> based on the specified message and <a href="/windows/desktop/SecGloss/s-gly">security context</a>.

The <b>SpMakeSignature</b> function is the dispatch function for the 
<a href="/windows/desktop/api/sspi/nf-sspi-makesignature">MakeSignature</a> function of the 
<a href="/windows/desktop/SecAuthN/sspi">Security Support Provider Interface</a>.

## -parameters

### -param ContextId [in]

A handle to the security context to be used to generate the message signature.


### -param fQOP [in]

Specifies package-specific flags that indicate the quality of protection. A security package can use this parameter to support the selection of cryptographic algorithms

### -param Message [in]

Pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure. On input, the structure contains the message to be signed.



### -param MessageSeqNo [in]

Sequence number to assign to the message. Sequence numbers are optional and are used as protection against loss and insertion of messages. A value of zero indicates that sequence numbers are not in use.



#### - MessageBuffers
## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed. The following  lists a common reason for failure and the error code that the function should return.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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

The counterpart to the <b>SpMakeSignature</b> function is the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-kspverifysignaturefn">SpVerifySignature</a> function, used to verify signatures at the receiving end.

SSP/APs must implement the <b>SpMakeSignature</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpMakeSignature</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-makesignature">MakeSignature</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-kspverifysignaturefn">SpVerifySignature</a>