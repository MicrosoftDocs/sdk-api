---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _LSA_TRANSLATED_NAME structure


## -description


The <b>LSA_TRANSLATED_NAME</b> structure is used with the 
<a href="https://msdn.microsoft.com/69051bad-91e7-469d-9010-48ac3d20f8af">LsaLookupSids</a> function to return information about the account identified by a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>.


## -struct-fields




### -field Use

A value from the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556744">SID_NAME_USE</a> enumeration that identifies the type of SID. 




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
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that contains the isolated name of the translated SID. An isolated name is a user, group, or local group account name without the domain name (for example, user_name, rather than Acctg\user_name).


### -field DomainIndex

Specifies the zero-based index of an entry in the 
<a href="https://msdn.microsoft.com/ddf0afcb-7ec4-42ed-bf40-38ef33f33a0c">LSA_REFERENCED_DOMAIN_LIST</a> structure returned by the 
<a href="https://msdn.microsoft.com/69051bad-91e7-469d-9010-48ac3d20f8af">LsaLookupSids</a> function. The entry contains the name and SID of the domain in which the account was found. 




If there is no corresponding domain for an account, this member contains a negative value.


## -see-also




<a href="https://msdn.microsoft.com/ddf0afcb-7ec4-42ed-bf40-38ef33f33a0c">LSA_REFERENCED_DOMAIN_LIST</a>



<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/69051bad-91e7-469d-9010-48ac3d20f8af">LsaLookupSids</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556744">SID_NAME_USE</a>
 

 

