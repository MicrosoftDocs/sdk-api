---
UID: NC:ntsecpkg.KspVerifySignatureFn
title: KspVerifySignatureFn (ntsecpkg.h)
description: Verifies that the message received is correct according to the signature.
helpviewer_keywords: ["KspVerifySignatureFn","KspVerifySignatureFn callback","SpVerifySignature","SpVerifySignature callback function [Security]","_ssp_spverifysignature","ntsecpkg/SpVerifySignature","security.spverifysignature"]
old-location: security\spverifysignature.htm
tech.root: security
ms.assetid: 62a74a1d-c7e6-4722-af57-997a5ff553ee
ms.date: 12/05/2018
ms.keywords: KspVerifySignatureFn, KspVerifySignatureFn callback, SpVerifySignature, SpVerifySignature callback function [Security], _ssp_spverifysignature, ntsecpkg/SpVerifySignature, security.spverifysignature
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
 - KspVerifySignatureFn
 - ntsecpkg/KspVerifySignatureFn
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
 - SpVerifySignature
---

# KspVerifySignatureFn callback function


## -description

Verifies that the message received is correct according to the <a href="/windows/desktop/SecGloss/d-gly">signature</a>.

The <b>SpVerifySignature</b> function is the dispatch function for the 
<a href="/windows/desktop/api/sspi/nf-sspi-verifysignature">VerifySignature</a> function of the 
<a href="/windows/desktop/SecAuthN/sspi">Security Support Provider Interface</a>.

## -parameters

### -param  [in]

A handle to the <a href="/windows/desktop/SecGloss/s-gly">security context</a> used to sign the message.


### -param Message [in]

Pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure containing the message to verify.


### -param MessageSeqNo [in]

Sequence number to assign to the message. Sequence numbers are optional and are used as protection against loss and insertion of messages. A value of zero indicates that sequence numbers are not in use.


### -param pfQOP [out]

Pointer to package-specific flags that indicate the quality of protection.


## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed. The following table lists a common reason for failure and the error code that the function should return.

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

The signature verified by the <b>SpVerifySignature</b> function is created by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-kspmakesignaturefn">SpMakeSignature</a> function, used by a message sender.

SSP/APs must implement the <b>SpVerifySignature</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpVerifySignature</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-makesignature">MakeSignature</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-kspmakesignaturefn">SpMakeSignature</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a>



<a href="/windows/desktop/api/sspi/nf-sspi-verifysignature">VerifySignature</a>