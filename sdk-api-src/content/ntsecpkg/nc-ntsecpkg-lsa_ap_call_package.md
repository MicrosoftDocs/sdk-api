---
UID: NC:ntsecpkg.LSA_AP_CALL_PACKAGE
title: LSA_AP_CALL_PACKAGE (ntsecpkg.h)
description: Called by the Local Security Authority (LSA) when a logon application with a trusted connection to the LSA calls the LsaCallAuthenticationPackage function and specifies the authentication package's identifier.
helpviewer_keywords: ["LSA_AP_CALL_PACKAGE","LSA_AP_CALL_PACKAGE callback","LsaApCallPackage","LsaApCallPackage callback function [Security]","_lsa_lsaapcallpackage","ntsecpkg/LsaApCallPackage","security.lsaapcallpackage"]
old-location: security\lsaapcallpackage.htm
tech.root: security
ms.assetid: be0f9886-c0f6-4361-96c7-d16da8713fc7
ms.date: 12/05/2018
ms.keywords: LSA_AP_CALL_PACKAGE, LSA_AP_CALL_PACKAGE callback, LsaApCallPackage, LsaApCallPackage callback function [Security], _lsa_lsaapcallpackage, ntsecpkg/LsaApCallPackage, security.lsaapcallpackage
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
 - LSA_AP_CALL_PACKAGE
 - ntsecpkg/LSA_AP_CALL_PACKAGE
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
 - LsaApCallPackage
---

# LSA_AP_CALL_PACKAGE callback function


## -description

Called by the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) when a logon application with a trusted connection to the LSA calls the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> function and specifies the authentication package's identifier.

<b>LsaApCallPackage</b> is called for logon applications only; calls from applications that do not have the SeTcbPrivilege privilege are routed to the specified authentication package's 
<a href="/previous-versions/windows/desktop/legacy/aa378218(v=vs.85)">LsaApCallPackageUntrusted</a> function instead.

## -parameters

### -param ClientRequest [in]

Pointer to an opaque 
<a href="/windows/desktop/SecAuthN/plsa-client-request">LSA_CLIENT_REQUEST</a> buffer representing the LSA client's request.

### -param ProtocolSubmitBuffer [in]

Supplies a protocol message specific to the authentication package.

### -param ClientBufferBase [in]

Provides the address within the client process of the protocol message. This may be necessary to remap any pointers within the <i>ProtocolSubmitBuffer</i> buffer.

### -param SubmitBufferLength [in]

Specifies the length of the <i>ProtocolSubmitBuffer</i> buffer, in bytes.

### -param ProtocolReturnBuffer [out]

Returns the address of the output buffer within the client process. The authentication package is responsible for calling the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_client_buffer">AllocateClientBuffer</a> function to allocate the buffer within the client process. The contents of this buffer are specific to the authentication package.

### -param ReturnBufferLength [out]

Pointer to a <b>ULONG</b> that returns the length of the <i>ProtocolReturnBuffer</i> buffer, in bytes.

### -param ProtocolStatus [out]

Pointer to an NTSTATUS value. If the function returns STATUS_SUCCESS, <i>ProtocolStatus</i> returns a completion status set by the authentication package. <i>ProtocolStatus</i> values are specific to the authentication package. 




More information about NTSTATUS codes can be found in the Subauth.h file shipped with the Platform SDK.

## -returns

If the function succeeds, return STATUS_SUCCESS. This return value indicates that the authentication package attempted to provide the requested service. Use the <i>ProtocolStatus</i> parameter to return the completion status of the service request.

If the authentication package could not process the request and therefore did not attempt to provide the requested service, return an NTSTATUS code indicating the problem. This code can be the following value or one of the 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The client's memory quota is insufficient to allocate the output buffer.

</td>
</tr>
</table>

## -remarks

This function must be implemented by authentication packages.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_client_buffer">AllocateClientBuffer</a>



<a href="/previous-versions/windows/desktop/legacy/aa378218(v=vs.85)">LsaApCallPackageUntrusted</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>
