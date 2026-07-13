---
UID: NF:ntsecapi.LsaQueryTrustedDomainInfoByName
title: LsaQueryTrustedDomainInfoByName function (ntsecapi.h)
description: The LsaQueryTrustedDomainInfoByName function returns information about a trusted domain.
helpviewer_keywords: ["LsaQueryTrustedDomainInfoByName","LsaQueryTrustedDomainInfoByName function [Security]","TrustedDomainFullInformation","TrustedDomainInformationBasic","TrustedDomainInformationEx","TrustedDomainNameInformation","TrustedPasswordInformation","TrustedPosixInformation","_lsa_lsaquerytrusteddomaininfobyname","ntsecapi/LsaQueryTrustedDomainInfoByName","security.lsaquerytrusteddomaininfobyname"]
old-location: security\lsaquerytrusteddomaininfobyname.htm
tech.root: security
ms.assetid: d33d6cee-bd8b-49f4-8e65-07cdc65bec7c
ms.date: 12/05/2018
ms.keywords: LsaQueryTrustedDomainInfoByName, LsaQueryTrustedDomainInfoByName function [Security], TrustedDomainFullInformation, TrustedDomainInformationBasic, TrustedDomainInformationEx, TrustedDomainNameInformation, TrustedPasswordInformation, TrustedPosixInformation, _lsa_lsaquerytrusteddomaininfobyname, ntsecapi/LsaQueryTrustedDomainInfoByName, security.lsaquerytrusteddomaininfobyname
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
 - LsaQueryTrustedDomainInfoByName
 - ntsecapi/LsaQueryTrustedDomainInfoByName
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
 - LsaQueryTrustedDomainInfoByName
---

# LsaQueryTrustedDomainInfoByName function


## -description

The <b>LsaQueryTrustedDomainInfoByName</b> function returns information about a trusted domain.

## -parameters

### -param PolicyHandle [in]

A handle to a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. This handle must have the POLICY_VIEW_LOCAL_INFORMATION access right. For more information, see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

### -param TrustedDomainName [in]

String that contains the name of the trusted domain. This can either be the domain name or the flat name.

### -param InformationClass [in]

Specifies the type of information to retrieve. This parameter can be one of the following values.

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
Name of the trusted domain.

</td>
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
<td width="40%"><a id="TrustedPasswordInformation"></a><a id="trustedpasswordinformation"></a><a id="TRUSTEDPASSWORDINFORMATION"></a><dl>
<dt><b>TrustedPasswordInformation</b></dt>
</dl>
</td>
<td width="60%">
Returns the password on the outbound side of the trust.

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
<td width="40%"><a id="TrustedDomainInformationEx"></a><a id="trusteddomaininformationex"></a><a id="TRUSTEDDOMAININFORMATIONEX"></a><dl>
<dt><b>TrustedDomainInformationEx</b></dt>
</dl>
</td>
<td width="60%">
Extended trust information, including the basic information and DNS domain name, and attributes about the trust.

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

### -param Buffer [out]

Receives a pointer to the returned buffer that contains the requested information. The format and content of this buffer depend on the information class. For example, if <i>InformationClass</i> is set to TrustedDomainInformationEx, <i>Buffer</i> receives a pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_information_ex">TRUSTED_DOMAIN_INFORMATION_EX</a> structure. For more information, see 
<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-trusted_information_class">TRUSTED_INFORMATION_CLASS</a>. 




When you have finished using the buffer, free it by calling the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a> function.

## -returns

If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> value, which can be one of the following values or one of the 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Caller does not have the appropriate access to complete the operation. For a list of the required access types, see the description of the <i>InformationClass</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INSUFFICIENT_
RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
Insufficient system resources, such as memory, to complete the call.

</td>
</tr>
</table>
 

You can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> value to a Windows error code.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname">LsaSetTrustedDomainInfoByName</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_information_ex">TRUSTED_DOMAIN_INFORMATION_EX</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-trusted_information_class">TRUSTED_INFORMATION_CLASS</a>