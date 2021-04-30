---
UID: NC:ntsecpkg.LSA_AP_CALL_PACKAGE_PASSTHROUGH
title: LSA_AP_CALL_PACKAGE_PASSTHROUGH (ntsecpkg.h)
description: The dispatch function for pass-through logon requests sent to the LsaCallAuthenticationPackage function.
helpviewer_keywords: ["LSA_AP_CALL_PACKAGE_PASSTHROUGH","LSA_AP_CALL_PACKAGE_PASSTHROUGH callback","LsaApCallPackagePassthrough","LsaApCallPackagePassthrough callback function [Security]","_lsa_lsaapcallpackagepassthrough","ntsecpkg/LsaApCallPackagePassthrough","security.lsaapcallpackagepassthrough"]
old-location: security\lsaapcallpackagepassthrough.htm
tech.root: security
ms.assetid: 8563b99d-8cc9-43a5-a6ae-615883c87bc2
ms.date: 12/05/2018
ms.keywords: LSA_AP_CALL_PACKAGE_PASSTHROUGH, LSA_AP_CALL_PACKAGE_PASSTHROUGH callback, LsaApCallPackagePassthrough, LsaApCallPackagePassthrough callback function [Security], _lsa_lsaapcallpackagepassthrough, ntsecpkg/LsaApCallPackagePassthrough, security.lsaapcallpackagepassthrough
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
 - LSA_AP_CALL_PACKAGE_PASSTHROUGH
 - ntsecpkg/LSA_AP_CALL_PACKAGE_PASSTHROUGH
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
 - LsaApCallPackagePassthrough
---

# LSA_AP_CALL_PACKAGE_PASSTHROUGH callback function


## -description

The dispatch function for pass-through logon requests sent to the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> function.

## -parameters

### -param ClientRequest [in]

Pointer to an opaque 
<a href="/windows/desktop/SecAuthN/plsa-client-request">LSA_CLIENT_REQUEST</a> buffer representing the LSA client's request.

### -param ProtocolSubmitBuffer [in]

Supplies a protocol-specific message to the authentication package.

### -param ClientBufferBase [in]

Provides the address within the client process of the protocol message. This may be necessary to remap pointers within the <i>ProtocolSubmitBuffer</i>.

### -param SubmitBufferLength [in]

Specifies the length of the <i>ProtocolSubmitBuffer</i> buffer, in bytes.

### -param ProtocolReturnBuffer [out]

Returns the address of the output buffer in the client process. The authentication package is responsible for calling the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_client_buffer">AllocateClientBuffer</a> function to allocate the buffer in the client process. The contents of this buffer are specific to the authentication package.

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



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>
