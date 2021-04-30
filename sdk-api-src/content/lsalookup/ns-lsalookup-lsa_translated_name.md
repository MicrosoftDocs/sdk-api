---
UID: NS:lsalookup._LSA_TRANSLATED_NAME
title: LSA_TRANSLATED_NAME (lsalookup.h)
description: Used with the LsaLookupSids function to return information about the account identified by a SID.
helpviewer_keywords: ["*PLSA_TRANSLATED_NAME","LSA_TRANSLATED_NAME","LSA_TRANSLATED_NAME structure [Security]","PLSA_TRANSLATED_NAME","PLSA_TRANSLATED_NAME structure pointer [Security]","SidTypeDomain","SidTypeInvalid","SidTypeUnknown","SidTypeWellKnownGroup","_lsa_lsa_translated_name","lsalookup/LSA_TRANSLATED_NAME","lsalookup/PLSA_TRANSLATED_NAME","security.lsa_translated_name"]
old-location: security\lsa_translated_name.htm
tech.root: security
ms.assetid: edea8317-5cdf-4d1e-9e6d-fcf17b91adb7
ms.date: 12/05/2018
ms.keywords: '*PLSA_TRANSLATED_NAME, LSA_TRANSLATED_NAME, LSA_TRANSLATED_NAME structure [Security], PLSA_TRANSLATED_NAME, PLSA_TRANSLATED_NAME structure pointer [Security], SidTypeDomain, SidTypeInvalid, SidTypeUnknown, SidTypeWellKnownGroup, _lsa_lsa_translated_name, lsalookup/LSA_TRANSLATED_NAME, lsalookup/PLSA_TRANSLATED_NAME, security.lsa_translated_name'
req.header: lsalookup.h
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
targetos: Windows
req.typenames: LSA_TRANSLATED_NAME, *PLSA_TRANSLATED_NAME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LSA_TRANSLATED_NAME
 - lsalookup/_LSA_TRANSLATED_NAME
 - PLSA_TRANSLATED_NAME
 - lsalookup/PLSA_TRANSLATED_NAME
 - LSA_TRANSLATED_NAME
 - lsalookup/LSA_TRANSLATED_NAME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LsaLookup.h
api_name:
 - LSA_TRANSLATED_NAME
---

# LSA_TRANSLATED_NAME structure


## -description

The <b>LSA_TRANSLATED_NAME</b> structure is used with the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupsids">LsaLookupSids</a> function to return information about the account identified by a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>.

## -struct-fields

### -field Use

A value from the 
<a href="/windows/desktop/api/winnt/ne-winnt-sid_name_use">SID_NAME_USE</a> enumeration that identifies the type of SID. 




If <b>Use</b> has one of the following values, one or both of the <b>Name</b> or <b>DomainIndex</b> members of <b>LSA_TRANSLATED_NAME</b> is not valid. These members are valid if <b>Use</b> has any other value.

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
The <b>DomainIndex</b> member is valid, but the <b>Name</b> member is not valid and must be ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SidTypeInvalid"></a><a id="sidtypeinvalid"></a><a id="SIDTYPEINVALID"></a><dl>
<dt><b>SidTypeInvalid</b></dt>
</dl>
</td>
<td width="60%">
Both <b>DomainIndex</b> and <b>Name</b> are not valid and must be ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SidTypeUnknown"></a><a id="sidtypeunknown"></a><a id="SIDTYPEUNKNOWN"></a><dl>
<dt><b>SidTypeUnknown</b></dt>
</dl>
</td>
<td width="60%">
Both <b>DomainIndex</b> and <b>Name</b> are not valid and must be ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SidTypeWellKnownGroup"></a><a id="sidtypewellknowngroup"></a><a id="SIDTYPEWELLKNOWNGROUP"></a><dl>
<dt><b>SidTypeWellKnownGroup</b></dt>
</dl>
</td>
<td width="60%">
The <b>Name</b> member is valid, but the <b>DomainIndex</b> member is not valid and must be ignored.

</td>
</tr>
</table>

### -field Name

An 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that contains the isolated name of the translated SID. An isolated name is a user, group, or local group account name without the domain name (for example, user_name, rather than Acctg\user_name).

### -field DomainIndex

Specifies the zero-based index of an entry in the 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list">LSA_REFERENCED_DOMAIN_LIST</a> structure returned by the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupsids">LsaLookupSids</a> function. The entry contains the name and SID of the domain in which the account was found. 




If there is no corresponding domain for an account, this member contains a negative value.

## -see-also

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list">LSA_REFERENCED_DOMAIN_LIST</a>



<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupsids">LsaLookupSids</a>



<a href="/windows/desktop/api/winnt/ne-winnt-sid_name_use">SID_NAME_USE</a>