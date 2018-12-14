---
UID: NS:winnt._TOKEN_PRIVILEGES
title: TOKEN_PRIVILEGES
author: windows-sdk-content
description: Contains information about a set of privileges for an access token.
old-location: security\token_privileges.htm
tech.root: secauthz
ms.assetid: c9016511-740f-44f3-92ed-17cc518c6612
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PTOKEN_PRIVILEGES, PTOKEN_PRIVILEGES, PTOKEN_PRIVILEGES structure pointer [Security], SE_PRIVILEGE_ENABLED, SE_PRIVILEGE_ENABLED_BY_DEFAULT, SE_PRIVILEGE_REMOVED, SE_PRIVILEGE_USED_FOR_ACCESS, TOKEN_PRIVILEGES, TOKEN_PRIVILEGES structure [Security], _TOKEN_PRIVILEGES, _win32_token_privileges_str, security.token_privileges, winnt/PTOKEN_PRIVILEGES, winnt/TOKEN_PRIVILEGES"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
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
 - Winnt.h
api_name:
 - TOKEN_PRIVILEGES
product: Windows
targetos: Windows
req.typenames: TOKEN_PRIVILEGES, *PTOKEN_PRIVILEGES
req.redist: 
---

# TOKEN_PRIVILEGES structure


## -description


The <b>TOKEN_PRIVILEGES</b> structure contains information about a set of privileges for an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a>.


## -struct-fields




### -field PrivilegeCount

This must be set to the number of entries in the <b>Privileges</b> array.


### -field Privileges

Specifies an array of 
<a href="https://msdn.microsoft.com/f337b561-4b67-42a0-b8de-06f546bafb26">LUID_AND_ATTRIBUTES</a> structures. Each structure contains the 
<a href="https://msdn.microsoft.com/a812a46b-f23f-45b1-a6c6-48f931b78750">LUID</a> and attributes of a privilege. To get the name of the privilege associated with a  <b>LUID</b>, call the <a href="https://msdn.microsoft.com/580fb58f-1470-4389-9f07-8f37403e2bdf">LookupPrivilegeName</a> function, passing the address of the <b>LUID</b> as the value of the <i>lpLuid</i> parameter.

<div class="alert"><b>Important</b>  The constant<b> ANYSIZE_ARRAY</b> is defined as 1 in the public header Winnt.h. To create this array with more than one element, you must allocate sufficient memory for the structure to take into account additional elements.</div>
<div> </div>
The attributes of a privilege can be a combination of the following values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SE_PRIVILEGE_ENABLED"></a><a id="se_privilege_enabled"></a><dl>
<dt><b>SE_PRIVILEGE_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The privilege is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_PRIVILEGE_ENABLED_BY_DEFAULT"></a><a id="se_privilege_enabled_by_default"></a><dl>
<dt><b>SE_PRIVILEGE_ENABLED_BY_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The privilege is enabled by default.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_PRIVILEGE_REMOVED"></a><a id="se_privilege_removed"></a><dl>
<dt><b>SE_PRIVILEGE_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
Used to remove a privilege. For details, see <a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_PRIVILEGE_USED_FOR_ACCESS"></a><a id="se_privilege_used_for_access"></a><dl>
<dt><b>SE_PRIVILEGE_USED_FOR_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
The privilege was used to gain access to an object or service. This flag is used to identify the relevant privileges in a set passed by a client application that may contain unnecessary privileges.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a>



<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>



<a href="https://msdn.microsoft.com/a812a46b-f23f-45b1-a6c6-48f931b78750">LUID</a>



<a href="https://msdn.microsoft.com/f337b561-4b67-42a0-b8de-06f546bafb26">LUID_AND_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/580fb58f-1470-4389-9f07-8f37403e2bdf">LookupPrivilegeName</a>



<a href="https://msdn.microsoft.com/2ee5615c-f684-4062-a6cb-e43e9de3a2fb">PRIVILEGE_SET</a>



<a href="https://msdn.microsoft.com/a73d934a-1abf-4e60-bf0a-6c4629f28f7a">PrivilegeCheck</a>



<a href="https://msdn.microsoft.com/a424c583-bb71-4bda-a27f-2389b89104d8">PrivilegedServiceAuditAlarm</a>



<a href="https://msdn.microsoft.com/cdb8af74-540d-4059-ac64-6243f6aabaa6">SetTokenInformation</a>



<a href="https://msdn.microsoft.com/b87c942b-8e58-471d-8cdf-e46cdac647c4">TOKEN_CONTROL</a>



<a href="https://msdn.microsoft.com/29fb738f-1ecd-4b72-9aea-64698cd74c12">TOKEN_DEFAULT_DACL</a>



<a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a>



<a href="https://msdn.microsoft.com/cb606665-1266-4e71-a145-9b04bf157cdc">TOKEN_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/85617d56-ad46-40a3-a335-121f3c8edcc3">TOKEN_OWNER</a>



<a href="https://msdn.microsoft.com/d23ebe6c-36a3-434a-a0fa-fcdf50dd19a0">TOKEN_PRIMARY_GROUP</a>



<a href="https://msdn.microsoft.com/9c533327-e4a0-4852-828c-622d190b7d1e">TOKEN_SOURCE</a>



<a href="https://msdn.microsoft.com/7fcc4a46-1bac-49c1-a239-b466d3bf31d9">TOKEN_STATISTICS</a>



<a href="https://msdn.microsoft.com/51b6717e-3fda-4af4-8995-4ac571eae2fd">TOKEN_TYPE</a>



<a href="https://msdn.microsoft.com/5dd8172d-7b1a-4cc0-b667-5fe91d278393">TOKEN_USER</a>
 

 

