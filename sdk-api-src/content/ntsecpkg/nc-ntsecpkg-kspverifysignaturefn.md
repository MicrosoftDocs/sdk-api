---
UID: NC:ntsecpkg.KspVerifySignatureFn
title: KspVerifySignatureFn (ntsecpkg.h)
description: Verifies that the message received is correct according to the signature.
old-location: security\spverifysignature.htm
tech.root: SecAuthN
ms.assetid: 62a74a1d-c7e6-4722-af57-997a5ff553ee
ms.date: 12/05/2018
ms.keywords: KspVerifySignatureFn, KspVerifySignatureFn callback, SpVerifySignature, SpVerifySignature callback function [Security], _ssp_spverifysignature, ntsecpkg/SpVerifySignature, security.spverifysignature
f1_keywords:
- ntsecpkg/SpVerifySignature
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
- SpVerifySignature
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# KspVerifySignatureFn callback function


## -description


Verifies that the message received is correct according to the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">signature</a>.

The <b>SpVerifySignature</b> function is the dispatch function for the 
<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-verifysignature">VerifySignature</a> function of the 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthN/sspi">Security Support Provider Interface</a>.


## -parameters




### -param ContextId


### -param Message


### -param MessageSeqNo


### -param pfQOP








#### - ContextHandle [in]

A handle to the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security context</a> used to sign the message.


#### - MessageBuffers [in]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure containing the message to verify.


#### - MessageSequenceNumber [in]

Sequence number to assign to the message. Sequence numbers are optional and are used as protection against loss and insertion of messages. A value of zero indicates that sequence numbers are not in use.


#### - QualityOfProtection [out]

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
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-kspmakesignaturefn">SpMakeSignature</a> function, used by a message sender.

SSP/APs must implement the <b>SpVerifySignature</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpVerifySignature</b> function is available in the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-makesignature">MakeSignature</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-kspmakesignaturefn">SpMakeSignature</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-verifysignature">VerifySignature</a>
 

 

