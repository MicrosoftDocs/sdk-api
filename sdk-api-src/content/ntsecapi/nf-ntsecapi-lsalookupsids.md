---
UID: NF:ntsecapi.LsaLookupSids
title: LsaLookupSids function
author: windows-sdk-content
description: Looks up the names that correspond to an array of security identifiers (SIDs). If LsaLookupSids cannot find a name that corresponds to a SID, the function returns the SID in character form.
old-location: security\lsalookupsids.htm
tech.root: secmgmt
ms.assetid: 69051bad-91e7-469d-9010-48ac3d20f8af
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: LsaLookupSids, LsaLookupSids function [Security], _lsa_lsalookupsids, ntsecapi/LsaLookupSids, security.lsalookupsids
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
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
 - LsaLookupSids
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LsaLookupSids function


## -description


<p class="CCE_Message">[<b>LsaLookupSids</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6B30D1FF-35DC-44E8-A765-36A5761EC0CE">LsaLookupSids2</a>.]

The <b>LsaLookupSids</b> function looks up the names that correspond to an array of <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs). If <b>LsaLookupSids</b> cannot find a name that corresponds to a SID, the function returns the SID in character form.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. This handle must have the POLICY_LOOKUP_NAMES access right. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param Count [in]

Specifies the number of SIDs in the <i>Sids</i> array. This is also the number of entries returned in the <i>Names</i> array.


### -param Sids [in]

Pointer to an array of SID pointers to look up. The SIDs can be well-known SIDs, user, group, or local group account SIDs, or domain SIDs.


### -param ReferencedDomains [out]

Receives a pointer to a pointer to a <a href="https://msdn.microsoft.com/ddf0afcb-7ec4-42ed-bf40-38ef33f33a0c">LSA_REFERENCED_DOMAIN_LIST</a> structure. The <b>Domains</b> member of this structure is an array that contains an entry for each domain in which a SID was found. The entry for each domain contains the SID and flat name of the domain. For Windows domains, the flat name is the NetBIOS name. For links with non–Windows domains, the flat name is the identifying name of that domain, or it is <b>NULL</b>. 




When you no longer need the information, pass the returned pointer to 
<a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a>. This memory must be freed even when the function fails with the either of the error codes <b>STATUS_NONE_MAPPED</b> or <b>STATUS_SOME_NOT_MAPPED</b>


### -param Names [out]

Receives a pointer to an array of 
<a href="https://msdn.microsoft.com/edea8317-5cdf-4d1e-9e6d-fcf17b91adb7">LSA_TRANSLATED_NAME</a> structures. Each entry in the <i>Names</i> array contains the name information for the corresponding entry in the <i>Sids</i> array. For account SIDs, the <b>Name</b> member of each structure contains the isolated name of the account. For domain SIDs, the <b>Name</b> member is not valid. 




The <b>DomainIndex</b> member of each entry in the <i>Names</i> array is the index of an entry in the <b>Domains</b> array returned in the <i>ReferencedDomains</i> parameter. The index identifies the <b>Domains</b> array for the domain in which the SID was found.

When you no longer need the information, pass the returned pointer to 
<a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a>. This memory must be freed even when the function fails with the either of the error codes <b>STATUS_NONE_MAPPED</b> or <b>STATUS_SOME_NOT_MAPPED</b>


## -returns



If the function succeeds, the return value is one of the following <b>NTSTATUS</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SOME_NOT_MAPPED</b></dt>
</dl>
</td>
<td width="60%">
Some of the SIDs could not be translated. This is an informational-level return value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
All of the SIDs were found and successfully translated.

</td>
</tr>
</table>
 

If the function fails, the return value is an <b>NTSTATUS</b> code, which can be one of the following values or one of the 
<a href="management_return_values.htm">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NONE_MAPPED</b></dt>
</dl>
</td>
<td width="60%">
None of the SIDs were translated. This is an error-level return value.

</td>
</tr>
</table>
 

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> code to a Windows error code.




## -remarks



For account SIDs, the string returned in the <b>Name</b> member is the isolated name of the account (for example, user_name). If you need the composite name of the account (for example, Acctg\user_name), get the domain name from the <i>ReferencedDomains</i> buffer and append a backslash and the isolated name.

If the <b>LsaLookupSids</b> function cannot translate a SID, the function uses the following algorithm:

<ol>
<li>If the SID's domain is known, the <i>ReferencedDomains</i> buffer contains an entry for the domain, and the string returned in the <i>Names</i> parameter is a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> representation of the account's relative identifier (RID) from the SID.</li>
<li>If the SID's domain is not known, the string returned in the <i>Names</i> parameter is a Unicode representation of the entire SID, and there is no domain record for this SID in the <i>ReferencedDomains</i> buffer.</li>
</ol>
In addition to looking up SIDs for local accounts, local domain accounts, and explicitly trusted domain accounts, <b>LsaLookupSids</b> can look up SIDs for any account in any domain in the Windows forest, including SIDs that appear only in the <b>SIDhistory</b> field of an account in the forest. The <b>SIDhistory</b> field stores the former SIDs of an account that has been moved from another domain. To perform these searches, the function queries the global catalog of the forest. 




## -see-also




<a href="https://msdn.microsoft.com/ddf0afcb-7ec4-42ed-bf40-38ef33f33a0c">LSA_REFERENCED_DOMAIN_LIST</a>



<a href="https://msdn.microsoft.com/edea8317-5cdf-4d1e-9e6d-fcf17b91adb7">LSA_TRANSLATED_NAME</a>



<a href="https://msdn.microsoft.com/361bc962-1e97-4606-a835-cbce37692c55">LsaOpenPolicy</a>
 

 

