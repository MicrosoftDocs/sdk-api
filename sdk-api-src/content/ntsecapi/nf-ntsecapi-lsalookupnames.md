---
UID: NF:ntsecapi.LsaLookupNames
title: LsaLookupNames function (ntsecapi.h)
description: Retrieves the security identifiers (SIDs) that correspond to an array of user, group, or local group names.
helpviewer_keywords: ["LsaLookupNames","LsaLookupNames function [Security]","_lsa_lsalookupnames","ntsecapi/LsaLookupNames","security.lsalookupnames"]
old-location: security\lsalookupnames.htm
tech.root: security
ms.assetid: 867604aa-7a39-4da7-b189-a9183461e9a0
ms.date: 12/05/2018
ms.keywords: LsaLookupNames, LsaLookupNames function [Security], _lsa_lsalookupnames, ntsecapi/LsaLookupNames, security.lsalookupnames
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
 - LsaLookupNames
 - ntsecapi/LsaLookupNames
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
 - AdvApi32Legacy.dll
 - Ext-MS-Win-AdvAPI32-Lsa-L1-1-1.dll
api_name:
 - LsaLookupNames
---

# LsaLookupNames function


## -description

The <b>LsaLookupNames</b> function retrieves the <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs) that correspond to an array of user, group, or local group names.

The <b>LsaLookupNames</b> function is superseded by the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames2">LsaLookupNames2</a> function. Applications should use the <b>LsaLookupNames2</b> function to ensure future compatibility.

The <b>LsaLookupNames</b> function can also retrieve computer accounts.

## -parameters

### -param PolicyHandle [in]

A handle to a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. The handle must have the POLICY_LOOKUP_NAMES access right. For more information, see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

### -param Count [in]

Specifies the number of names in the <i>Names</i> array. This is also the number of entries returned in the <i>Sids</i> array. This value must be less than or equal to 1000.

### -param Names [in]

Pointer to an array of 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structures that contain the names to look up. The strings in these structures can be the names of user, group, or local group accounts, or the names of domains. Domain names can be DNS domain names or NetBIOS domain names. 




For more information about the format of the name strings, see Remarks.

### -param ReferencedDomains [out]

Receives a pointer to an 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list">LSA_REFERENCED_DOMAIN_LIST</a> structure. The <b>Domains</b> member of this structure is an array that contains an entry for each domain in which a name was found. The <b>DomainIndex</b> member of each entry in the <i>Sids</i> array is the index of the <b>Domains</b> array entry for the domain in which the name was found. 




When you have finished using the returned pointer, free the memory by calling the  
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a> function. This memory must be freed even when the function fails with the either of the error codes <b>STATUS_NONE_MAPPED</b> or <b>STATUS_SOME_NOT_MAPPED</b>

### -param Sids [out]

Receives a pointer to an array of 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_translated_sid">LSA_TRANSLATED_SID</a> structures. Each entry in the <i>Sids</i> array contains the SID information for the corresponding entry in the <i>Names</i> array.  




When you have finished using the returned pointer, free the memory by calling the  
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a> function. This memory must be freed even when the function fails with the either of the error codes <b>STATUS_NONE_MAPPED</b> or <b>STATUS_SOME_NOT_MAPPED</b>

## -returns

If the function succeeds, the function returns  one of the following <b>NTSTATUS</b> values.

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

<tr>
<td width="40%">
<dl>
<dt><b>STATUS_TOO_MANY_NAMES</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The Names array parameter was too large.
</td>
</tr>
</table>
 

Use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> code to a Windows error code.

## -remarks

> [!WARNING]
>Use fully qualified account names (for example, domain_name\user_name) instead of isolated names (for example, user_name). Fully qualified names are unambiguous and provide better performance when the lookup is performed. This function also supports fully qualified DNS names (for example, example.example.com\user_name) and <a href="/windows/desktop/SecGloss/u-gly">user principal names</a> (UPN) (for example, someone@example.com).

> [!WARNING]
>For more information about the limitations of isolated names, please refer to the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames2">LsaLookupNames2</a> documentation.

The <b>LsaLookupNames</b> function uses the following algorithm to translate account names.

<p class="proch"><b>To translate names</b>

<ol>
<li>If the name is a well-known name, such as Local or Interactive, the function returns the corresponding well-known <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).</li>
<li>If the name is the name of the built-in domain, the function returns the SID of that domain.</li>
<li>If the name is the name of the account domain, the function returns the SID of that domain.</li>
<li>If the name is the name of the primary domain, the function returns the SID of that domain.</li>
<li>If the name is one of the names of the trusted domain, the function returns the SID of that domain.</li>
<li>If the name is a user, group, or local group account in the built-in domain, the function returns the SID of that account.</li>
<li>If the name is a user, group, or local group account in the account domain on the local system, the function returns the SID of that account.</li>
<li>If the name is found in the cache, the function returns the SID of that account.
<li>If the name is a user, group, or a local group in the primary domain, the function returns the SID of that account.</li>
<li>After looking in the primary domain, the primary domain looks in each of its trusted domains.</li>
<li>Otherwise, the name is not translated.</li>
</ol>

In addition to looking up local accounts, local domain accounts, and explicitly trusted domain accounts, <b>LsaLookupNames</b> can look up the name of any account in any domain in the Windows forest.


#### Examples

For an example that calls this function, see 
<a href="/windows/desktop/SecMgmt/translating-between-names-and-sids">Translating Between Names and SIDs</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list">LSA_REFERENCED_DOMAIN_LIST</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_translated_sid">LSA_TRANSLATED_SID</a>



<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupsids">LsaLookupSids</a>