---
UID: NF:ntsecapi.LsaCallAuthenticationPackage
title: LsaCallAuthenticationPackage function (ntsecapi.h)
description: Used by a logon application to communicate with an authentication package.
helpviewer_keywords: ["LsaCallAuthenticationPackage","LsaCallAuthenticationPackage function [Security]","_lsa_lsacallauthenticationpackage","ntsecapi/LsaCallAuthenticationPackage","security.lsacallauthenticationpackage"]
old-location: security\lsacallauthenticationpackage.htm
tech.root: security
ms.assetid: b891fa60-28b3-4819-9a92-e4524677fa4f
ms.date: 12/05/2018
ms.keywords: LsaCallAuthenticationPackage, LsaCallAuthenticationPackage function [Security], _lsa_lsacallauthenticationpackage, ntsecapi/LsaCallAuthenticationPackage, security.lsacallauthenticationpackage
req.header: ntsecapi.h
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
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LsaCallAuthenticationPackage
 - ntsecapi/LsaCallAuthenticationPackage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - LsaCallAuthenticationPackage
---

# LsaCallAuthenticationPackage function


## -description

The <b>LsaCallAuthenticationPackage</b> function is used by a logon application to communicate with an authentication package.

This function is typically used to access services provided by the authentication package.

## -parameters

### -param LsaHandle [in]

A handle obtained from a previous call to 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaregisterlogonprocess">LsaRegisterLogonProcess</a> or 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaconnectuntrusted">LsaConnectUntrusted</a>.

### -param AuthenticationPackage [in]

Supplies the identifier of the authentication package. This value is obtained by calling 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupauthenticationpackage">LsaLookupAuthenticationPackage</a>.

### -param ProtocolSubmitBuffer [in]

An authentication package–specific message buffer passed to the authentication package.

For information about the format and content of this buffer, see the documentation for the individual authentication package.

### -param SubmitBufferLength [in]

Indicates the length, in bytes, of the <i>ProtocolSubmitBuffer</i> buffer.

### -param ProtocolReturnBuffer [out]

A pointer that receives the address of the buffer returned by the authentication package.

For information about the format and content of this buffer, see the documentation for the individual authentication package.

This buffer is allocated by this function. When you have finished using this buffer, free the memory by calling the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreereturnbuffer">LsaFreeReturnBuffer</a> function.

### -param ReturnBufferLength [out]

A pointer to a <b>ULONG</b> that receives the length of the returned buffer, in bytes.

### -param ProtocolStatus [out]

If the function succeeds, this parameter receives an <b>NTSTATUS</b> code that indicates the completion status of the authentication package.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS. Check the <i>ProtocolStatus</i> parameter to obtain the status returned by the authentication package.

If the function fails, the return value is an <b>NTSTATUS</b> code. The following are possible error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
The call could not be completed because the client's memory quota is not sufficient to allocate the return buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_PACKAGE</b></dt>
</dl>
</td>
<td width="60%">
The specified authentication package is not recognized by the LSA.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_PKINIT_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The Kerberos client received a KDC certificate that is not valid. For device logon, strict KDC validation is required, so the KDC must have certificates that use the "Kerberos Authentication" template or equivalent. Also the KDC certificate could be expired, revoked, or the client is under active attack of sending requests to the wrong server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_PKINIT_CLIENT_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The Kerberos client is using a system certificate that is not valid. For device logon, there must be a DNS name. Also, the system certificate could be expired or the wrong one could be selected.

</td>
</tr>
</table>
 

For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an <b>NTSTATUS</b> code to a Windows error code.

## -remarks

Logon applications can call <b>LsaCallAuthenticationPackage</b> to communicate with an authentication package. There are several reasons why an application may do this:

<ul>
<li>To implement multiple-message authentication protocols, such as the NTLM Challenge-Response protocol.</li>
<li>To pass state change information to the authentication package. For example, the NTLM might notify the MSV1_0 package that a previously unreachable domain controller is now reachable. The authentication package would then re-logon any users logged on to that domain controller.</li>
</ul>
Typically, this function is used to exchange information with a custom authentication package. This function is not needed by an application that is using one of the authentication packages supplied with Windows, such as MSV1_0 or Kerberos.

You must call <b>LsaCallAuthenticationPackage</b> to clean up PKINIT device credentials for LOCAL_SYSTEM and NETWORK_SERVICE. When there is no PKINIT device credential, a successful call does no operation. When there is a PKINIT device credential, a successful call cleans up the PKINIT device credential so that only the password credential remains.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreereturnbuffer">LsaFreeReturnBuffer</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupauthenticationpackage">LsaLookupAuthenticationPackage</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a>
