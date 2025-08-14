---
UID: NF:ntsecapi.LsaCreateTrustedDomainEx
title: LsaCreateTrustedDomainEx function (ntsecapi.h)
description: The LsaCreateTrustedDomainEx function establishes a new trusted domain by creating a new TrustedDomain object.
helpviewer_keywords: ["LsaCreateTrustedDomainEx","LsaCreateTrustedDomainEx function [Security]","_lsa_lsacreatetrusteddomainex","ntsecapi/LsaCreateTrustedDomainEx","security.lsacreatetrusteddomainex"]
old-location: security\lsacreatetrusteddomainex.htm
tech.root: security
ms.assetid: 2f458098-9498-4f08-bd13-ac572678d734
ms.date: 12/05/2018
ms.keywords: LsaCreateTrustedDomainEx, LsaCreateTrustedDomainEx function [Security], _lsa_lsacreatetrusteddomainex, ntsecapi/LsaCreateTrustedDomainEx, security.lsacreatetrusteddomainex
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LsaCreateTrustedDomainEx
 - ntsecapi/LsaCreateTrustedDomainEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-advapi32-lsa-l1-1-4.dll
 - ext-ms-win-advapi32-lsa-l1-1-3.dll
 - ext-ms-win-advapi32-lsa-l1-1-2.dll
 - Advapi32.dll
api_name:
 - LsaCreateTrustedDomainEx
---

# LsaCreateTrustedDomainEx function


## -description

The <b>LsaCreateTrustedDomainEx</b> function establishes a new trusted domain by creating a new <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object.

## -parameters

### -param PolicyHandle [in]

A handle to a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. For the object to be created, the caller must have permission to create children on the <b>System</b> container. For information about policy object handles, see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

### -param TrustedDomainInformation [in]

Pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_information_ex">TRUSTED_DOMAIN_INFORMATION_EX</a> structure that contains the name and SID of the new trusted domain.

### -param AuthenticationInformation [in]

Pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_auth_information">TRUSTED_DOMAIN_AUTH_INFORMATION</a> structure that contains authentication information for the new trusted domain.

### -param DesiredAccess [in]

An 
<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> structure that specifies the accesses to be granted for the new trusted domain.

### -param TrustedDomainHandle [out]

Receives the LSA policy handle of the remote trusted domain. You can pass this handle into LSA function calls to manage the LSA policy of the trusted domain. 




When your application no longer needs this handle, it should call 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaclose">LsaClose</a> to delete the handle.

## -returns

If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> code, which can be one of the following values or one of the 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_DIRECTORY_SERVICE_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
 The target system (specified in the <i>TrustedDomainInformation</i> parameter) for the <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object is not a domain controller.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_SID</b></dt>
</dl>
</td>
<td width="60%">
The specified SID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_UNSUCCESSFUL</b></dt>
</dl>
</td>
<td width="60%">
Unable to determine whether the target system is a domain controller.

</td>
</tr>
</table>
 

You can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> code to a Windows error code.

## -remarks

<b>LsaCreateTrustedDomainEx</b> does not check whether the specified domain name matches the specified SID or whether the SID and name represent an actual domain.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaclose">LsaClose</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsadeletetrusteddomain">LsaDeleteTrustedDomain</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname">LsaSetTrustedDomainInfoByName</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation">LsaSetTrustedDomainInformation</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_auth_information">TRUSTED_DOMAIN_AUTH_INFORMATION</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_information_ex">TRUSTED_DOMAIN_INFORMATION_EX</a>