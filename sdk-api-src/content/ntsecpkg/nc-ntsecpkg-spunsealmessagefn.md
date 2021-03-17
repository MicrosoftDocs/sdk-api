---
UID: NC:ntsecpkg.SpUnsealMessageFn
title: SpUnsealMessageFn (ntsecpkg.h)
description: Decrypts a message that was previously encrypted with the SpSealMessage function.
helpviewer_keywords: ["SpUnsealMessage","SpUnsealMessage callback function [Security]","SpUnsealMessageFn","SpUnsealMessageFn callback","_ssp_spunsealmessage","ntsecpkg/SpUnsealMessage","security.spunsealmessage"]
old-location: security\spunsealmessage.htm
tech.root: security
ms.assetid: 3ece6f30-bb8b-4fad-a8c4-9088c134cf25
ms.date: 12/05/2018
ms.keywords: SpUnsealMessage, SpUnsealMessage callback function [Security], SpUnsealMessageFn, SpUnsealMessageFn callback, _ssp_spunsealmessage, ntsecpkg/SpUnsealMessage, security.spunsealmessage
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
 - SpUnsealMessageFn
 - ntsecpkg/SpUnsealMessageFn
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
 - SpUnsealMessage
---

# SpUnsealMessageFn callback function


## -description

Decrypts a message that was previously encrypted with the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spsealmessagefn">SpSealMessage</a> function.

The <b>SpUnsealMessage</b> function is the dispatch function for the 
<a href="/windows/desktop/api/sspi/nf-sspi-decryptmessage">DecryptMessage (General)</a> function of the 
<a href="/windows/desktop/SecAuthN/sspi">Security Support Provider Interface</a>.

## -parameters

### -param ContextHandle [in]

Handle of the <a href="/windows/desktop/SecGloss/s-gly">security context</a> used to seal the message.

### -param MessageBuffers [in]

Pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure that contains the message buffers and a signature buffer.

### -param MessageSequenceNumber [in]

Sequence number to assign to the message. Sequence numbers are optional and are used as protection against loss and insertion of messages. A value of zero indicates that sequence numbers are not in use.

### -param QualityOfProtection [out]

Not used.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.

## -remarks

SSP/APs must implement the <b>SpUnsealMessage</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpUnsealMessage</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-decryptmessage">DecryptMessage (General)</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spsealmessagefn">SpSealMessage</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a>