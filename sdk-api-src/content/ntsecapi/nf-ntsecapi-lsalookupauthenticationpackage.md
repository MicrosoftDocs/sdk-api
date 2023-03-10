---
UID: NF:ntsecapi.LsaLookupAuthenticationPackage
title: LsaLookupAuthenticationPackage function (ntsecapi.h)
description: Obtains the unique identifier of an authentication package.
helpviewer_keywords: ["LsaLookupAuthenticationPackage","LsaLookupAuthenticationPackage function [Security]","MICROSOFT_KERBEROS_NAME_A","MSV1_0_PACKAGE_NAME","NEGOSSP_NAME_A","_lsa_lsalookupauthenticationpackage","ntsecapi/LsaLookupAuthenticationPackage","security.lsalookupauthenticationpackage"]
old-location: security\lsalookupauthenticationpackage.htm
tech.root: security
ms.assetid: c6504aea-fdba-44ac-b2dc-070707bb1183
ms.date: 12/05/2018
ms.keywords: LsaLookupAuthenticationPackage, LsaLookupAuthenticationPackage function [Security], MICROSOFT_KERBEROS_NAME_A, MSV1_0_PACKAGE_NAME, NEGOSSP_NAME_A, _lsa_lsalookupauthenticationpackage, ntsecapi/LsaLookupAuthenticationPackage, security.lsalookupauthenticationpackage
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
 - LsaLookupAuthenticationPackage
 - ntsecapi/LsaLookupAuthenticationPackage
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
 - LsaLookupAuthenticationPackage
---

# LsaLookupAuthenticationPackage function


## -description

The <b>LsaLookupAuthenticationPackage</b> function obtains the unique identifier of an authentication package.

## -parameters

### -param LsaHandle [in]

Handle obtained from a previous call to 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaregisterlogonprocess">LsaRegisterLogonProcess</a> or 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaconnectuntrusted">LsaConnectUntrusted</a>.

### -param PackageName [in]

Pointer to an 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_string">LSA_STRING</a> structure that specifies the name of the authentication package. The package name must not exceed 127 bytes in length. The following table lists the names of the Microsoft-provided authentication packages.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_PACKAGE_NAME"></a><a id="msv1_0_package_name"></a><dl>
<dt><b>MSV1_0_PACKAGE_NAME</b></dt>
</dl>
</td>
<td width="60%">
ANSI version of the MSV1_0 authentication package name.

</td>
</tr>
<tr>
<td width="40%"><a id="MICROSOFT_KERBEROS_NAME_A"></a><a id="microsoft_kerberos_name_a"></a><dl>
<dt><b>MICROSOFT_KERBEROS_NAME_A</b></dt>
</dl>
</td>
<td width="60%">
ANSI version of the Kerberos authentication package name.

</td>
</tr>
<tr>
<td width="40%"><a id="NEGOSSP_NAME_A"></a><a id="negossp_name_a"></a><dl>
<dt><b>NEGOSSP_NAME_A</b></dt>
</dl>
</td>
<td width="60%">
ANSI version of the Negotiate authentication package name.

</td>
</tr>
</table>

### -param AuthenticationPackage [out]

Pointer to a <b>ULONG</b> that receives the authentication package identifier.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. The following are possible error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_PACKAGE</b></dt>
</dl>
</td>
<td width="60%">
The specified authentication package is unknown to the LSA.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NAME_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
The authentication package name exceeds 127 bytes.

</td>
</tr>
</table>
 

For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.

## -remarks

The authentication package identifier is used in calls to authentication functions such as 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> and 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>