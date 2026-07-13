---
UID: NF:ntsecapi.LsaSetTrustedDomainInformation
title: LsaSetTrustedDomainInformation function (ntsecapi.h)
description: The LsaSetTrustedDomainInformation function modifies a Policy object's information about a trusted domain.
helpviewer_keywords: ["LsaSetTrustedDomainInformation","LsaSetTrustedDomainInformation function [Security]","TrustedDomainNameInformation","TrustedPasswordInformation","TrustedPosixOffsetInformation","_lsa_lsasettrusteddomaininformation","ntsecapi/LsaSetTrustedDomainInformation","security.lsasettrusteddomaininformation"]
old-location: security\lsasettrusteddomaininformation.htm
tech.root: security
ms.assetid: a7b89ea7-af92-46ba-ac73-2fba1cc27680
ms.date: 12/05/2018
ms.keywords: LsaSetTrustedDomainInformation, LsaSetTrustedDomainInformation function [Security], TrustedDomainNameInformation, TrustedPasswordInformation, TrustedPosixOffsetInformation, _lsa_lsasettrusteddomaininformation, ntsecapi/LsaSetTrustedDomainInformation, security.lsasettrusteddomaininformation
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
 - LsaSetTrustedDomainInformation
 - ntsecapi/LsaSetTrustedDomainInformation
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
 - LsaSetTrustedDomainInformation
---

# LsaSetTrustedDomainInformation function


## -description

The <b>LsaSetTrustedDomainInformation</b> function modifies a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object's information about a trusted domain.

## -parameters

### -param PolicyHandle [in]

A handle to the <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object of a domain controller. The required user rights for this handle depend on the value of the <i>InformationClass</i> parameter. For more information, see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

### -param TrustedDomainSid [in]

Pointer to the SID of the trusted domain whose information is modified. If the <i>InformationClass</i> parameter is set to TrustedDomainNameInformation, this parameter must point to the SID of the domain to add to the list of trusted domains.

### -param InformationClass [in]

Specifies one of the following values from the 
<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-trusted_information_class">TRUSTED_INFORMATION_CLASS</a> enumeration type. The value indicates the type of information being set. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TrustedDomainNameInformation"></a><a id="trusteddomainnameinformation"></a><a id="TRUSTEDDOMAINNAMEINFORMATION"></a><dl>
<dt><b>TrustedDomainNameInformation</b></dt>
</dl>
</td>
<td width="60%">
If the specified domain is not in the list of trusted domains, the 
<b>LsaSetTrustedDomainInformation</b> function adds it. The <i>TrustedDomainSid</i> parameter must be the SID of the domain to add. The <i>Buffer</i> parameter must be a pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_name_info">TRUSTED_DOMAIN_NAME_INFO</a> structure containing the name of the domain to add.  




If the specified domain is already in the list of trusted domains, the function fails.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedPosixOffsetInformation"></a><a id="trustedposixoffsetinformation"></a><a id="TRUSTEDPOSIXOFFSETINFORMATION"></a><dl>
<dt><b>TrustedPosixOffsetInformation</b></dt>
</dl>
</td>
<td width="60%">
Sets the value used to generate Posix user and group identifiers. The <i>Buffer</i> parameter must be a pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_posix_offset_info">TRUSTED_POSIX_OFFSET_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedPasswordInformation"></a><a id="trustedpasswordinformation"></a><a id="TRUSTEDPASSWORDINFORMATION"></a><dl>
<dt><b>TrustedPasswordInformation</b></dt>
</dl>
</td>
<td width="60%">
Sets the password for the trusted domain. The <i>Buffer</i> parameter must be a pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_password_info">TRUSTED_PASSWORD_INFO</a> structure containing the old and new passwords for the specified domain. The handle passed in the <i>PolicyHandle</i> parameter must have the POLICY_CREATE_SECRET access right. The old password string can be <b>NULL</b>.

</td>
</tr>
</table>

### -param Buffer [in]

Pointer to a structure containing the information to set. The type of structure depends on the value of the <i>InformationClass</i> parameter.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

You can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsadeletetrusteddomain">LsaDeleteTrustedDomain</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_name_info">TRUSTED_DOMAIN_NAME_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-trusted_information_class">TRUSTED_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_password_info">TRUSTED_PASSWORD_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_posix_offset_info">TRUSTED_POSIX_OFFSET_INFO</a>