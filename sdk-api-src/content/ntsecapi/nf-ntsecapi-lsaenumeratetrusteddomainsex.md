---
UID: NF:ntsecapi.LsaEnumerateTrustedDomainsEx
title: LsaEnumerateTrustedDomainsEx function (ntsecapi.h)
description: Returns information about the domains trusted by the local system.
helpviewer_keywords: ["LsaEnumerateTrustedDomainsEx","LsaEnumerateTrustedDomainsEx function [Security]","_lsa_lsaenumeratetrusteddomainsex","ntsecapi/LsaEnumerateTrustedDomainsEx","security.lsaenumeratetrusteddomainsex"]
old-location: security\lsaenumeratetrusteddomainsex.htm
tech.root: security
ms.assetid: 4a203bff-c3e1-4d95-b556-617dc8c2e8c2
ms.date: 12/05/2018
ms.keywords: LsaEnumerateTrustedDomainsEx, LsaEnumerateTrustedDomainsEx function [Security], _lsa_lsaenumeratetrusteddomainsex, ntsecapi/LsaEnumerateTrustedDomainsEx, security.lsaenumeratetrusteddomainsex
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
 - LsaEnumerateTrustedDomainsEx
 - ntsecapi/LsaEnumerateTrustedDomainsEx
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
 - LsaEnumerateTrustedDomainsEx
---

# LsaEnumerateTrustedDomainsEx function


## -description

The <b>LsaEnumerateTrustedDomainsEx</b> function returns information about the domains trusted by the local system.<b>LsaEnumerateTrustedDomainsEx</b> returns information only on direct trusts. 
<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsenumeratedomaintrustsa">DsEnumerateDomainTrusts</a> is recommended for more complete trust enumeration purposes.

## -parameters

### -param PolicyHandle [in]

A handle to a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. This call requires POLICY_VIEW_LOCAL_INFORMATION access to the <b>Policy</b> object. For more information, see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

### -param EnumerationContext [in]

A pointer to an 
<a href="/windows/desktop/SecMgmt/lsa-enumeration-handle">LSA_ENUMERATION_HANDLE</a> that you can use to make multiple calls to <b>LsaEnumerateTrustedDomainsEx</b>  to retrieve all of the trusted domain information. For more information, see Remarks.

### -param Buffer [out]

Pointer to a buffer that receives a list of 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_information_ex">TRUSTED_DOMAIN_INFORMATION_EX</a> structures that contain information about the enumerated trusted domains. 




Your application should free this buffer when it is no longer needed by calling 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a>.

### -param PreferedMaximumLength [in]

Preferred maximum length, in bytes, of returned data. This is not a hard upper limit, but serves as a guide. Due to data conversion between systems with different natural data sizes, the actual amount of data returned may be greater than this value.

### -param CountReturned [out]

Pointer to a <b>LONG</b> that receives the number of trusted domain objects returned.

## -returns

If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an  <b>NTSTATUS</b> code, which can be one of the following values or one of the 
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
Caller does not have the appropriate access to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MORE_ENTRIES</b></dt>
</dl>
</td>
<td width="60%">
There are no more entries. This warning is returned if no objects have been enumerated because the <i>EnumerationContext</i> value is too high.

</td>
</tr>
</table>
 

You can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> code to a Windows error code.

## -remarks

Retrieving all trust information may require more than a single <b>LsaEnumerateTrustedDomainsEx</b> call.

<p class="proch"><b>To use the <i>EnumerationContext</i> parameter to make multiple calls</b>

<ol>
<li>Set the variable pointed to by <i>EnumerationContext</i> to zero.</li>
<li>If <b>LsaEnumerateTrustedDomainsEx</b> returns STATUS_SUCCESS or STATUS_MORE_ENTRIES, call the function again, passing in the <i>EnumerationContext</i> value returned by the previous call.</li>
<li>The enumeration is complete when the function returns STATUS_NO_MORE_ENTRIES.</li>
</ol>

## -see-also

<a href="/windows/desktop/SecMgmt/lsa-enumeration-handle">LSA_ENUMERATION_HANDLE</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_information_ex">TRUSTED_DOMAIN_INFORMATION_EX</a>