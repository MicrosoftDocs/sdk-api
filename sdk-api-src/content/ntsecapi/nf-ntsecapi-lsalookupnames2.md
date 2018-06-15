---
UID: NF:ntsecapi.LsaLookupNames2
title: LsaLookupNames2 function
author: windows-sdk-content
description: Retrieves the security identifiers (SIDs) for specified account names. LsaLookupNames2 can look up the SID for any account in any domain in a Windows forest.
old-location: security\lsalookupnames2.htm
old-project: SecMgmt
ms.assetid: fe219070-6a00-4b8c-b2e4-2ad290a1cb9c
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: LSA_LOOKUP_ISOLATED_AS_LOCAL, LsaLookupNames2, LsaLookupNames2 function [Security], _lsa_lsalookupnames2, ntsecapi/LsaLookupNames2, security.lsalookupnames2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-lsapolicy-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-LSAPolicy-L1-1-1.dll
api_name:
 - LsaLookupNames2
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LsaLookupNames2 function


## -description


The <b>LsaLookupNames2</b> function retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs) for specified account names. <b>LsaLookupNames2</b> can look up the SID for any account in any domain in a Windows forest.

The <a href="https://msdn.microsoft.com/867604aa-7a39-4da7-b189-a9183461e9a0">LsaLookupNames</a> function is superseded by the <b>LsaLookupNames2</b> function. Applications should use the <b>LsaLookupNames2</b> function to ensure future compatibility.

This function differs from the 
<a href="https://msdn.microsoft.com/867604aa-7a39-4da7-b189-a9183461e9a0">LsaLookupNames</a> function in that <b>LsaLookupNames2</b> returns each SID as a single element, while <b>LsaLookupNames</b> divides each SID into an RID/domain pair.


## -parameters




### -param PolicyHandle [in]

A handle to a 
<a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. The handle must have the POLICY_LOOKUP_NAMES access right. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>. 


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
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structures that contain the names to look up. These strings can be the names of user, group, or local group accounts, or the names of domains. Domain names can be DNS domain names or NetBIOS domain names. 




For more information about the format of the name strings, see Remarks.


### -param ReferencedDomains [out]

Receives a pointer to an 
<a href="https://msdn.microsoft.com/ddf0afcb-7ec4-42ed-bf40-38ef33f33a0c">LSA_REFERENCED_DOMAIN_LIST</a> structure. The <b>Domains</b> member of this structure is an array that contains an entry for each domain in which a name was found. The <b>DomainIndex</b> member of each entry in the <i>Sids</i> array is the index of the <b>Domains</b> array entry for the domain in which the name was found.

When you have finished using the returned pointer, free it by calling the  
<a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a> function. This memory must be freed even when the function fails with the either of the error codes <b>STATUS_NONE_MAPPED</b> or <b>STATUS_SOME_NOT_MAPPED</b>


### -param Sids [out]

Receives a pointer to an array of 
<a href="https://msdn.microsoft.com/792de958-8e24-46d8-b484-159435bc96e3">LSA_TRANSLATED_SID2</a> structures. Each entry in the <i>Sids</i> array contains the SID information for the corresponding entry in the <i>Names</i> array. 




When you have finished using the returned pointer, free it by calling the  
<a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a> function. This memory must be freed even when the function fails with the either of the error codes <b>STATUS_NONE_MAPPED</b> or <b>STATUS_SOME_NOT_MAPPED</b>


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
<a href="https://docs.microsoft.com/windows/desktop//SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

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
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> code to a Windows error code.




## -remarks



Use fully qualified account names (for example, <i>DomainName</i>\<i>UserName</i>) instead of isolated names (for example, <i>UserName</i>). Fully qualified names are unambiguous and provide better performance when the lookup is performed. This function also supports fully qualified DNS names (for example, <i>Example</i>.<i>Example</i>.com\<i>UserName</i>) and <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal names</a> (UPN) (for example, <i>Someone</i>@<i>Example</i>.com).

Translation of isolated names introduces the possibility of name collisions because the same name may be used in multiple domains. The <b>LsaLookupNames2</b> function uses the following algorithm to translate isolated names.

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To translate isolated names</b>

<ol>
<li>If the name is a well-known name, such as Local or Interactive, the function returns the corresponding well-known <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).</li>
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




<a href="https://msdn.microsoft.com/ddf0afcb-7ec4-42ed-bf40-38ef33f33a0c">LSA_REFERENCED_DOMAIN_LIST</a>



<a href="https://msdn.microsoft.com/792de958-8e24-46d8-b484-159435bc96e3">LSA_TRANSLATED_SID2</a>



<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a>
 

 

