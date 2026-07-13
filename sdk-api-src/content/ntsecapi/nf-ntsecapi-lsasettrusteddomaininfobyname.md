---
UID: NF:ntsecapi.LsaSetTrustedDomainInfoByName
title: LsaSetTrustedDomainInfoByName function (ntsecapi.h)
description: The LsaSetTrustedDomainInfoByName function sets values for a TrustedDomain object.
helpviewer_keywords: ["LsaSetTrustedDomainInfoByName","LsaSetTrustedDomainInfoByName function [Security]","TrustedDomainAuthInformation","TrustedDomainFullInformation","TrustedDomainInformationEx","TrustedPosixInformation","_lsa_lsasettrusteddomaininfobyname","ntsecapi/LsaSetTrustedDomainInfoByName","security.lsasettrusteddomaininfobyname"]
old-location: security\lsasettrusteddomaininfobyname.htm
tech.root: security
ms.assetid: 263e1025-1010-463d-8bc7-cdf916ce9872
ms.date: 12/05/2018
ms.keywords: LsaSetTrustedDomainInfoByName, LsaSetTrustedDomainInfoByName function [Security], TrustedDomainAuthInformation, TrustedDomainFullInformation, TrustedDomainInformationEx, TrustedPosixInformation, _lsa_lsasettrusteddomaininfobyname, ntsecapi/LsaSetTrustedDomainInfoByName, security.lsasettrusteddomaininfobyname
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
 - LsaSetTrustedDomainInfoByName
 - ntsecapi/LsaSetTrustedDomainInfoByName
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
 - LsaSetTrustedDomainInfoByName
---

# LsaSetTrustedDomainInfoByName function


## -description

The <b>LsaSetTrustedDomainInfoByName</b> function sets values for a 
<a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object.

## -parameters

### -param PolicyHandle [in]

A handle to a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. The <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> of the trusted domain object determines whether the caller's changes are accepted. For information about policy object handles, see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

### -param TrustedDomainName [in]

Name of the trusted domain to set values for. This can either be the domain name or the flat name.

### -param InformationClass [in]

Specifies the type of information to set. Specify one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TrustedPosixInformation"></a><a id="trustedposixinformation"></a><a id="TRUSTEDPOSIXINFORMATION"></a><dl>
<dt><b>TrustedPosixInformation</b></dt>
</dl>
</td>
<td width="60%">
Posix offset of the trusted domain.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedDomainInformationEx"></a><a id="trusteddomaininformationex"></a><a id="TRUSTEDDOMAININFORMATIONEX"></a><dl>
<dt><b>TrustedDomainInformationEx</b></dt>
</dl>
</td>
<td width="60%">
Extended trust information, including the basic information and DNS domain name, and attributes about the trust.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedDomainAuthInformation"></a><a id="trusteddomainauthinformation"></a><a id="TRUSTEDDOMAINAUTHINFORMATION"></a><dl>
<dt><b>TrustedDomainAuthInformation</b></dt>
</dl>
</td>
<td width="60%">
Authentication information for the trust, including authentication information for both the inbound and outbound side of the trust (if it exists).

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedDomainFullInformation"></a><a id="trusteddomainfullinformation"></a><a id="TRUSTEDDOMAINFULLINFORMATION"></a><dl>
<dt><b>TrustedDomainFullInformation</b></dt>
</dl>
</td>
<td width="60%">
Full information, including the Posix offset and the authentication information.

</td>
</tr>
</table>

### -param Buffer [in]

Pointer to a structure that contains the information to set. The type of structure depends on the value of the <i>InformationClass</i> parameter.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
the "LSA Policy Function Return Values" section of <a href="/windows/desktop/SecMgmt/management-return-values">Security Management Return Values</a>.

You can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname">LsaQueryTrustedDomainInfoByName</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_information_ex">TRUSTED_DOMAIN_INFORMATION_EX</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-trusted_information_class">TRUSTED_INFORMATION_CLASS</a>