---
UID: NF:ntsecapi.LsaEnumerateTrustedDomains
title: LsaEnumerateTrustedDomains function (ntsecapi.h)
description: The LsaEnumerateTrustedDomains function retrieves the names and SIDs of domains trusted to authenticate logon credentials.
helpviewer_keywords: ["LsaEnumerateTrustedDomains","LsaEnumerateTrustedDomains function [Security]","_lsa_lsaenumeratetrusteddomains","ntsecapi/LsaEnumerateTrustedDomains","security.lsaenumeratetrusteddomains"]
old-location: security\lsaenumeratetrusteddomains.htm
tech.root: security
ms.assetid: 5c371d5a-26cf-4a99-a8e1-006b6b3cc91f
ms.date: 12/05/2018
ms.keywords: LsaEnumerateTrustedDomains, LsaEnumerateTrustedDomains function [Security], _lsa_lsaenumeratetrusteddomains, ntsecapi/LsaEnumerateTrustedDomains, security.lsaenumeratetrusteddomains
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
 - LsaEnumerateTrustedDomains
 - ntsecapi/LsaEnumerateTrustedDomains
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-security-lsalookup-l2-1-0.dll
 - API-MS-Win-security-lsalookup-l2-1-1.dll
 - API-MS-Win-Security-LSALookup-L2-1-2.dll
api_name:
 - LsaEnumerateTrustedDomains
---

# LsaEnumerateTrustedDomains function


## -description

The <b>LsaEnumerateTrustedDomains</b> function retrieves the names and SIDs of domains trusted to authenticate logon <a href="/windows/desktop/SecGloss/c-gly">credentials</a>. <b>LsaEnumerateTrustedDomains</b> is intended for use on systems running Windows NT 4.0 or earlier versions of Windows NT. Use 
<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsenumeratedomaintrustsa">DsEnumerateDomainTrusts</a> for any other trust enumeration purpose. Specifically, <b>LsaEnumerateTrustedDomains</b> can only be used if one or more of the following is true:
<ul>
<li>The calling system is running Windows NT 4.0 or an earlier version of Windows NT.</li>
<li>The target system (specified using the <i>PolicyHandle</i> parameter), is a domain controller running Windows NT 4.0 or an earlier version.</li>
<li>The calling system is running Windows NT 4.0 or earlier version and is not a domain controller, and the target system is a domain controller in the calling system's domain. The target system can be running any version of Windows NT, including Windows 2000 and Windows XP.</li>
</ul>

## -parameters

### -param PolicyHandle [in]

A handle to a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. The handle must have the POLICY_VIEW_LOCAL_INFORMATION access right. For more information, see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

### -param EnumerationContext [in]

Pointer to an enumeration handle that enables you to make multiple calls to enumerate all the trusted domains. On the first call to <b>LsaEnumerateTrustedDomains</b>, <i>EnumerationContext</i> must point to a variable that has been initialized to zero. On subsequent calls to <b>LsaEnumerateTrustedDomains</b>, <i>EnumerationContext</i> must point to the enumeration handle returned by the previous call.

### -param Buffer [out]

Receives a pointer to an array of 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information">LSA_TRUST_INFORMATION</a> structures that contain the names and SIDs of one or more trusted domains. 




When you no longer need the information, pass the returned pointer to 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a>.

### -param PreferedMaximumLength [in]

Specifies the preferred maximum size, in bytes, of the returned buffer. This information is approximate; the actual number of bytes returned may be greater than this value.

### -param CountReturned [out]

Pointer to a variable that receives the number of elements returned in the <i>Buffer</i> parameter.

## -returns

If the function is successful, the return value is one of the following NTSTATUS values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The enumeration has been successfully completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_MORE_ENTRIES</b></dt>
</dl>
</td>
<td width="60%">
The call was successful, but there are more trusted domains to be enumerated. Call <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomains">LsaEnumerateTrustedDomains</a> again, passing the value returned in the <i>EnumerationContext</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MORE_ENTRIES</b></dt>
</dl>
</td>
<td width="60%">
There are no more trusted domains to enumerate.

</td>
</tr>
</table>
 

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

You can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.

## -remarks

For domains with domain controllers running only Windows NT 4.0 or earlier versions of Windows NT, <b>LsaEnumerateTrustedDomains</b> returns a list of all trusted domains. In releases of Windows NT up to and including release 4.0, all trusted domains are directly trusted.

In Windows XP and Windows 2000 mixed-mode domains, domain controllers may be running Windows XP, Windows 2000, or Windows NT. Therefore, in mixed-mode domains, some trusted domains are directly trusted and others are indirectly trusted. When enumerating the trusted domains of a system in a mixed-mode domain, <b>LsaEnumerateTrustedDomains</b> returns only directly trusted domains.

In contrast, Windows XP and Windows 2000 native-mode domains contain only Windows 2000 domain controllers, even though there may be members in the domain running Windows NT 4.0 or earlier versions. When enumerating the trusted domains of a system in a native-mode Windows XP and Windows 2000 domain, <b>LsaEnumerateTrustedDomains</b> returns both directly trusted and indirectly trusted domains.

Retrieving all trust information may require more than a single <b>LsaEnumerateTrustedDomains</b> call. You can use the <i>EnumerationContext</i> parameter to make multiple calls, as follows: On the first call, set the variable pointed to by <i>EnumerationContext</i> to zero. If <b>LsaEnumerateTrustedDomains</b> returns STATUS_SUCCESS or STATUS_MORE_ENTRIES, call the function again, passing in the <i>EnumerationContext</i> value returned by the previous call. The enumeration is complete when the function returns STATUS_NO_MORE_ENTRIES.

## -see-also

<b>LSA_TRUST_INFORMATION</b>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex">LsaEnumerateTrustedDomainsEx</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy">LsaOpenPolicy</a>