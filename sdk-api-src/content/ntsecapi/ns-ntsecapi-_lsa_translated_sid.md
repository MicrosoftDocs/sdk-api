---
UID: NS:ntsecapi._LSA_TRANSLATED_SID
title: "_LSA_TRANSLATED_SID"
author: windows-sdk-content
description: Used with the LsaLookupNames function to return information about the SID that identifies an account.
old-location: security\lsa_translated_sid.htm
tech.root: secmgmt
ms.assetid: 1fa8fb74-3e61-4982-aa6b-a0ffe979abd4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PLSA_TRANSLATED_SID, LSA_TRANSLATED_SID, LSA_TRANSLATED_SID structure [Security], PLSA_TRANSLATED_SID, PLSA_TRANSLATED_SID structure pointer [Security], SidTypeDomain, SidTypeInvalid, SidTypeUnknown, _LSA_TRANSLATED_SID, _lsa_lsa_translated_sid, ntsecapi/LSA_TRANSLATED_SID, ntsecapi/PLSA_TRANSLATED_SID, security.lsa_translated_sid"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - LSA_TRANSLATED_SID
product: Windows
targetos: Windows
req.typenames: LSA_TRANSLATED_SID, *PLSA_TRANSLATED_SID
req.redist: 
---

# _LSA_TRANSLATED_SID structure


## -description


The <b>LSA_TRANSLATED_SID</b> structure is used with the 
<a href="https://msdn.microsoft.com/867604aa-7a39-4da7-b189-a9183461e9a0">LsaLookupNames</a> function to return information about the 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> that identifies an account.


## -struct-fields




### -field Use

A value from the 
<a href="https://msdn.microsoft.com/4e6af6bd-056b-4f5a-b223-57a673c3fcfa">SID_NAME_USE</a> enumeration type that identifies the type of SID. 




If <b>Use</b> has one of the following values, one or both of the <b>RelativeId</b> or <b>DomainIndex</b> members of <b>LSA_TRANSLATED_SID</b> is not valid. These members are valid if <b>Use</b> has any other value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SidTypeDomain"></a><a id="sidtypedomain"></a><a id="SIDTYPEDOMAIN"></a><dl>
<dt><b>SidTypeDomain</b></dt>
</dl>
</td>
<td width="60%">
The <b>DomainIndex</b> member is valid, but the <b>RelativeId</b> member is not valid and must be ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SidTypeInvalid"></a><a id="sidtypeinvalid"></a><a id="SIDTYPEINVALID"></a><dl>
<dt><b>SidTypeInvalid</b></dt>
</dl>
</td>
<td width="60%">
Both <b>DomainIndex</b> and <b>RelativeId</b> are not valid and must be ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SidTypeUnknown"></a><a id="sidtypeunknown"></a><a id="SIDTYPEUNKNOWN"></a><dl>
<dt><b>SidTypeUnknown</b></dt>
</dl>
</td>
<td width="60%">
Both <b>DomainIndex</b> and <b>RelativeId</b> members are not valid and must be ignored.

</td>
</tr>
</table>
 


### -field RelativeId

Specifies the relative identifier (RID) of the account's SID. The RID identifies the account relative to the domain referenced by the <b>DomainIndex</b> member. The account's complete SID consists of the domain SID followed by the RID.


### -field DomainIndex

Specifies the zero-based index of an entry in the 
<a href="https://msdn.microsoft.com/ddf0afcb-7ec4-42ed-bf40-38ef33f33a0c">LSA_REFERENCED_DOMAIN_LIST</a> structure returned by the <a href="https://msdn.microsoft.com/867604aa-7a39-4da7-b189-a9183461e9a0">LsaLookupNames</a> function. This entry contains the name and SID of the domain in which the account was found. 




If there is no corresponding domain for an account, this member contains a negative value.


## -see-also




<a href="https://msdn.microsoft.com/ddf0afcb-7ec4-42ed-bf40-38ef33f33a0c">LSA_REFERENCED_DOMAIN_LIST</a>



<a href="https://msdn.microsoft.com/867604aa-7a39-4da7-b189-a9183461e9a0">LsaLookupNames</a>



<a href="https://msdn.microsoft.com/4e6af6bd-056b-4f5a-b223-57a673c3fcfa">SID_NAME_USE</a>
 

 

