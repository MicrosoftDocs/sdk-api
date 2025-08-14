---
UID: NF:ntsecapi.LsaQueryTrustedDomainInfo
title: LsaQueryTrustedDomainInfo function (ntsecapi.h)
description: The LsaQueryTrustedDomainInfo function retrieves information about a trusted domain.
helpviewer_keywords: ["LsaQueryTrustedDomainInfo","LsaQueryTrustedDomainInfo function [Security]","TrustedDomainFullInformation","TrustedDomainInformationBasic","TrustedDomainInformationEx","TrustedDomainNameInformation","TrustedPasswordInformation","TrustedPosixOffsetInformation","_lsa_lsaquerytrusteddomaininfo","ntsecapi/LsaQueryTrustedDomainInfo","security.lsaquerytrusteddomaininfo"]
old-location: security\lsaquerytrusteddomaininfo.htm
tech.root: security
ms.assetid: 62925515-a6f3-4b5f-bf97-edb968af19a3
ms.date: 12/05/2018
ms.keywords: LsaQueryTrustedDomainInfo, LsaQueryTrustedDomainInfo function [Security], TrustedDomainFullInformation, TrustedDomainInformationBasic, TrustedDomainInformationEx, TrustedDomainNameInformation, TrustedPasswordInformation, TrustedPosixOffsetInformation, _lsa_lsaquerytrusteddomaininfo, ntsecapi/LsaQueryTrustedDomainInfo, security.lsaquerytrusteddomaininfo
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
 - LsaQueryTrustedDomainInfo
 - ntsecapi/LsaQueryTrustedDomainInfo
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
 - LsaQueryTrustedDomainInfo
---

# LsaQueryTrustedDomainInfo function


## -description

The <b>LsaQueryTrustedDomainInfo</b> function retrieves information about a trusted domain.

## -parameters

### -param PolicyHandle [in]

A handle to the <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object of a domain controller that has a trust relationship with the domain identified by the <i>TrustedDomainSid</i> parameter. The handle must have the POLICY_VIEW_LOCAL_INFORMATION access right. For more information, see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

### -param TrustedDomainSid [in]

Pointer to the SID of the trusted domain to query.

### -param InformationClass [in]

Specifies one of the following values from the 
<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-trusted_information_class">TRUSTED_INFORMATION_CLASS</a> enumeration type. The value indicates the type of information being requested. 




					

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
Retrieves the name of the trusted domain. The <i>Buffer</i> parameter receives a pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_name_info">TRUSTED_DOMAIN_NAME_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedPosixOffsetInformation"></a><a id="trustedposixoffsetinformation"></a><a id="TRUSTEDPOSIXOFFSETINFORMATION"></a><dl>
<dt><b>TrustedPosixOffsetInformation</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the value used to generate Posix user and group identifiers for the trusted domain. The <i>Buffer</i> parameter receives a pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_posix_offset_info">TRUSTED_POSIX_OFFSET_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedPasswordInformation"></a><a id="trustedpasswordinformation"></a><a id="TRUSTEDPASSWORDINFORMATION"></a><dl>
<dt><b>TrustedPasswordInformation</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the password for the trusted domain. The <i>Buffer</i> parameter receives a pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_password_info">TRUSTED_PASSWORD_INFO</a> structure. The handle passed in the <i>PolicyHandle</i> parameter must have the POLICY_GET_PRIVATE_INFORMATION access right.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedDomainInformationEx"></a><a id="trusteddomaininformationex"></a><a id="TRUSTEDDOMAININFORMATIONEX"></a><dl>
<dt><b>TrustedDomainInformationEx</b></dt>
</dl>
</td>
<td width="60%">
Retrieves extended information for the trusted domain. The <i>Buffer</i> parameter receives a pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_information_ex">TRUSTED_DOMAIN_INFORMATION_EX</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedDomainInformationBasic"></a><a id="trusteddomaininformationbasic"></a><a id="TRUSTEDDOMAININFORMATIONBASIC"></a><dl>
<dt><b>TrustedDomainInformationBasic</b></dt>
</dl>
</td>
<td width="60%">
This value is not supported.
							

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedDomainFullInformation"></a><a id="trusteddomainfullinformation"></a><a id="TRUSTEDDOMAINFULLINFORMATION"></a><dl>
<dt><b>TrustedDomainFullInformation</b></dt>
</dl>
</td>
<td width="60%">
Retrieves complete information for the trusted domain. This information includes the Posix offset information, authentication information, and the extended information returned for the TrustedDomainInformationEx value. The <i>Buffer</i> parameter receives a pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_full_information">TRUSTED_DOMAIN_FULL_INFORMATION</a> structure.

</td>
</tr>
</table>

### -param Buffer [out]

A pointer to a buffer that receives a pointer to a structure that contains the requested information. The type of structure depends on the value of the <i>InformationClass</i> parameter. 




When you have finished using the information, free the returned pointer by passing it to 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a>.

## -returns

If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> value that indicates the error. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

You can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> value to a Windows error code.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation">LsaSetTrustedDomainInformation</a>



<a href="/windows/desktop/api/lsalookup/ns-lsalookup-policy_account_domain_info">POLICY_ACCOUNT_DOMAIN_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_audit_events_info">POLICY_AUDIT_EVENTS_INFO</a>



<a href="/windows/desktop/api/lsalookup/ns-lsalookup-policy_dns_domain_info">POLICY_DNS_DOMAIN_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_lsa_server_role_info">POLICY_LSA_SERVER_ROLE_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_modification_info">POLICY_MODIFICATION_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_primary_domain_info">POLICY_PRIMARY_DOMAIN_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-trusted_information_class">TRUSTED_INFORMATION_CLASS</a>