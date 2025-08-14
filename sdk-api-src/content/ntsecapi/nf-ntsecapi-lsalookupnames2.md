---
UID: NF:ntsecapi.LsaLookupNames2
title: LsaLookupNames2 function (ntsecapi.h)
description: Retrieves the security identifiers (SIDs) for specified account names. LsaLookupNames2 can look up the SID for any account in any domain in a Windows forest.
old-location: security\lsalookupnames2.htm
tech.root: SecMgmt
ms.assetid: fe219070-6a00-4b8c-b2e4-2ad290a1cb9c
ms.date: 12/05/2018
ms.keywords: LSA_LOOKUP_ISOLATED_AS_LOCAL, LsaLookupNames2, LsaLookupNames2 function [Security], _lsa_lsalookupnames2, ntsecapi/LsaLookupNames2, security.lsalookupnames2
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
 - LsaLookupNames2
 - ntsecapi/LsaLookupNames2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-lsapolicy-l1-1-2.dll
 - Advapi32.dll
 - API-MS-Win-Security-lsapolicy-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-LSAPolicy-L1-1-1.dll
api_name:
 - LsaLookupNames2
---

# LsaLookupNames2 function


## -description

The <b>LsaLookupNames2</b> function retrieves the <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs) for specified account names. <b>LsaLookupNames2</b> can look up the SID for any account in any domain in a Windows forest.

The <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames">LsaLookupNames</a> function is superseded by the <b>LsaLookupNames2</b> function. Applications should use the <b>LsaLookupNames2</b> function to ensure future compatibility.

This function differs from the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames">LsaLookupNames</a> function in that <b>LsaLookupNames2</b> returns each SID as a single element, while <b>LsaLookupNames</b> divides each SID into an RID/domain pair.

## -parameters

### -param PolicyHandle [in]

A handle to a 
<a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. The handle must have the POLICY_LOOKUP_NAMES access right. For more information, see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

### -param Flags [in]

Values that control the behavior of this function. The following value is currently defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LSA_LOOKUP_ISOLATED_AS_LOCAL"></a><a id="lsa_lookup_isolated_as_local"></a><dl>
<dt><b>LSA_LOOKUP_ISOLATED_AS_LOCAL</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
The function searches only on the local systems for names that do not specify a domain. The function does search on remote systems for names that do specify a domain.

</td>
</tr>
</table>

### -param Count [in]

Specifies the number of names in the <i>Names</i> array. This is also the number of entries returned in the <i>Sids</i> array.

### -param Names [in]

Pointer to an array of 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structures that contain the names to look up. These strings can be the names of user, group, or local group accounts, or the names of domains. Domain names can be DNS domain names or NetBIOS domain names. 




For more information about the format of the name strings, see Remarks.

### -param ReferencedDomains [out]

Receives a pointer to an 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list">LSA_REFERENCED_DOMAIN_LIST</a> structure. The <b>Domains</b> member of this structure is an array that contains an entry for each domain in which a name was found. The <b>DomainIndex</b> member of each entry in the <i>Sids</i> array is the index of the <b>Domains</b> array entry for the domain in which the name was found.

When you have finished using the returned pointer, free it by calling the  
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a> function. This memory must be freed even when the function fails with the either of the error codes <b>STATUS_NONE_MAPPED</b> or <b>STATUS_SOME_NOT_MAPPED</b>

### -param Sids [out]

Receives a pointer to an array of 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_translated_sid2">LSA_TRANSLATED_SID2</a> structures. Each entry in the <i>Sids</i> array contains the SID information for the corresponding entry in the <i>Names</i> array. 




When you have finished using the returned pointer, free it by calling the  
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a> function. This memory must be freed even when the function fails with the either of the error codes <b>STATUS_NONE_MAPPED</b> or <b>STATUS_SOME_NOT_MAPPED</b>

## -returns

If the function succeeds, the function returns one of the following <b>NTSTATUS</b> values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SOME_NOT_MAPPED</b></dt>
</dl>
</td>
<td width="60%">
Some of the names could not be translated. This is an informational-level return value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
All of the names were found and successfully translated.

</td>
</tr>
</table>
 

If the function fails, the return value is the following <b>NTSTATUS</b> value or one of the 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NONE_MAPPED</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
None of the names were translated.

</td>
</tr>
</table>
 

Use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> code to a Windows error code.

## -remarks

Use fully qualified account names (for example, <i>DomainName</i>&#92;<i>UserName</i>) instead of isolated names (for example, <i>UserName</i>). Fully qualified names are unambiguous and provide better performance when the lookup is performed. This function also supports fully qualified DNS names (for example, <i>Example</i>.<i>Example</i>.com&#92;<i>UserName</i>) and <a href="/windows/desktop/SecGloss/u-gly">user principal names</a> (UPN) (for example, <i>Someone</i>@<i>Example</i>.com).

Translation of isolated names introduces the possibility of name collisions because the same name may be used in multiple domains. The <b>LsaLookupNames2</b> function uses the following algorithm to translate isolated names.

<p class="proch"><b>To translate isolated names</b>

<ol>
<li>If the name is a well-known name, such as Local or Interactive, the function returns the corresponding well-known <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).</li>
<li>If the name is the name of the built-in domain, the function returns the SID of that domain.</li>
<li>If the name is the name of the account domain, the function returns the SID of that domain.</li>
<li>If the name is the name of the primary domain, the function returns the SID of that domain.</li>
<li>If the name is one of the names of the trusted domain, the function returns the SID of that domain.</li>
<li>If the name is a user, group, or local group account in the built-in domain, the function returns the SID of that account.</li>
<li>If the name is a user, group, or local group account in the account domain on the local system, the function returns the SID of that account.</li>
<li>If the name is a user, group, or a local group in the primary domain, the function returns the SID of that account.</li>
<li>After looking in the primary domain, the function looks in each of the primary domain's trusted domains.</li>
<li>Otherwise, the name is not translated.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list">LSA_REFERENCED_DOMAIN_LIST</a>



<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_translated_sid2">LSA_TRANSLATED_SID2</a>



<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a>
