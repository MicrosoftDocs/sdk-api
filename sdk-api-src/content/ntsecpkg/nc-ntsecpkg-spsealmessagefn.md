---
UID: NC:ntsecpkg.SpSealMessageFn
title: SpSealMessageFn (ntsecpkg.h)
description: Encrypts a message exchanged between a client and server.
helpviewer_keywords: ["SpSealMessage","SpSealMessageFn","SpSealMessageFn callback","SpSealMessageFn callback function [Security]","TBD","_ssp_spsealmessage","ntsecpkg/SpSealMessageFn","security.spsealmessage"]
old-location: security\spsealmessage.htm
tech.root: security
ms.assetid: 400bc3e7-e9a1-4267-b4de-44d79dceb9e5
ms.date: 12/05/2018
ms.keywords: SpSealMessage, SpSealMessageFn, SpSealMessageFn callback, SpSealMessageFn callback function [Security], TBD, _ssp_spsealmessage, ntsecpkg/SpSealMessageFn, security.spsealmessage
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
 - SpSealMessageFn
 - ntsecpkg/SpSealMessageFn
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
 - SpSealMessageFn
---

# SpSealMessageFn callback function


## -description

Encrypts a message exchanged between a client and server.

The <b>SpSealMessage</b> function is the dispatch function for the 
<a href="/windows/desktop/api/sspi/nf-sspi-encryptmessage">EncryptMessage (General)</a> function of the 
<a href="/windows/desktop/SecAuthN/sspi">Security Support Provider Interface</a>.

## -parameters

### -param ContextHandle [in]

Handle of the <a href="/windows/desktop/SecGloss/s-gly">security context</a> used to sign the message.

### -param QualityOfProtection [in]

Specifies package-specific flags that indicate the quality of protection. An SSP/AP can use this parameter to enable the selection of cryptographic algorithms.

### -param MessageBuffers [in, out]

Pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure that contains message buffers. Only one of these message buffers can be of type SECBUFFER_DATA, and it contains the message to be encrypted. The buffer cannot have the SECBUFFER_READONLY attribute because the encryption is done in-place.

### -param MessageSequenceNumber [in]

Sequence number to assign to the message. Sequence numbers are optional and are used as protection against loss and insertion of messages. A value of zero indicates that sequence numbers are not in use.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed. The following table lists common reasons for failure and the error codes that the function should return.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The context could not be found or was not configured for message integrity.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The signature buffer could not be found or was too small.

</td>
</tr>
</table>

## -remarks

Messages encrypted by the sender using the <b>SpSealMessage</b> function are decrypted using the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spunsealmessagefn">SpUnsealMessage</a> function.

SSP/APs must implement the <b>SpSealMessage</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpSealMessage</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spunsealmessagefn">SpUnsealMessage</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a>