---
UID: NF:subauth.Msv1_0SubAuthenticationRoutineGeneric
title: Msv1_0SubAuthenticationRoutineGeneric function (subauth.h)
description: Performs Remote Access Service authentication when subauthentication is requested by calling the LsaCallAuthenticationPackage function.
helpviewer_keywords: ["Msv1_0SubAuthenticationRoutineGeneric","Msv1_0SubAuthenticationRoutineGeneric function [Security]","security.msv1_0subauthenticationroutinegeneric","subauth/Msv1_0SubAuthenticationRoutineGeneric"]
old-location: security\msv1_0subauthenticationroutinegeneric.htm
tech.root: security
ms.assetid: 78F51B69-DCFA-47D0-84C5-B44C79D50DAF
ms.date: 12/05/2018
ms.keywords: Msv1_0SubAuthenticationRoutineGeneric, Msv1_0SubAuthenticationRoutineGeneric function [Security], security.msv1_0subauthenticationroutinegeneric, subauth/Msv1_0SubAuthenticationRoutineGeneric
req.header: subauth.h
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
 - Msv1_0SubAuthenticationRoutineGeneric
 - subauth/Msv1_0SubAuthenticationRoutineGeneric
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Subauth.h
api_name:
 - Msv1_0SubAuthenticationRoutineGeneric
---

# Msv1_0SubAuthenticationRoutineGeneric function


## -description

Performs <a href="/windows/desktop/RRAS/portal">Remote Access Service</a> authentication when subauthentication is requested by calling the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> function.

The <a href="/windows/desktop/SecGloss/s-gly">security principal's</a> credentials and information from the <a href="/windows/desktop/SecGloss/s-gly">Security Accounts Manager</a> (SAM) database are passed to this function for authentication.

This function is implemented by custom subauthentication package DLLs for use with the MSV1_0 authentication package.

This function is called only for a 
<a href="/windows/desktop/SecAuthN/noninteractive-authentication">noninteractive authentication</a>, only on the authenticating server where the account resides, and only if a subauthentication DLL is registered under the correct key in the registry.

## -parameters

### -param SubmitBuffer

A pointer to a buffer that contains a <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-msv1_0_subauth_request">MSV1_0_SUBAUTH_REQUEST</a> structure that contains the  authentication information to be submitted.

### -param SubmitBufferLength

The  size, in bytes, of the <i>SubmitBuffer</i> buffer.

### -param ReturnBufferLength [out]

The size, in bytes, of the <i>ReturnBuffer</i> buffer.

### -param ReturnBuffer [out]

A pointer to a buffer that contains a <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-msv1_0_subauth_response">MSV1_0_SUBAUTH_RESPONSE</a> structure that contains the response from the subauthentication package.

## -returns

If the function succeeds, the return value is <b>STATUS_SUCCESS</b>.

If the function fails, the return value is an NTSTATUS code.

## -see-also

<a href="/windows/desktop/api/subauth/nf-subauth-msv1_0subauthenticationroutine">Msv1_0SubAuthenticationRoutine</a>