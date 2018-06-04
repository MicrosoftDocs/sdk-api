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

# AuditSetPerUserPolicy function


## -description


The <b>AuditSetPerUserPolicy</b> function sets per-user audit policy in one or more audit subcategories for the specified principal. 


## -parameters




### -param pSid [in]

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure associated with the principal for which to set  audit policy. Per-user policy for group SIDs is not currently supported.


### -param pAuditPolicy [in]

A pointer to an array of <a href="https://msdn.microsoft.com/3fafeec9-a028-4a65-933e-fb973eb257b0">AUDIT_POLICY_INFORMATION</a> structures. Each structure specifies per-user audit policy for one audit subcategory.

The <b>AuditCategoryGuid</b> member of these structures is ignored.


### -param dwPolicyCount

TBD




#### - PolicyCount [in]

The number of elements in the <i>pAuditPolicy</i> array.


## -returns




						If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. <b>GetLastError</b> may return one of the following error codes defined in WinError.h.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The caller does not have the privilege or access rights necessary to call this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
<dt>87</dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_USER</b></dt>
<dt>1317</dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure specified by the <i>pSID</i> parameter is not associated with an existing user.

</td>
</tr>
</table>
 




## -remarks



To successfully call this function, the caller must have <b>SeSecurityPrivilege</b> or have <b>AUDIT_SET_USER_POLICY</b> access on the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Audit security object</a>.




## -see-also




<a href="https://msdn.microsoft.com/7d4790de-ebd6-4840-b532-7158b8d80db2">AuditQueryPerUserPolicy</a>



<a href="https://msdn.microsoft.com/5c268033-65fd-4a74-90a1-4b9e1e18daf1">AuditQuerySystemPolicy</a>



<a href="https://msdn.microsoft.com/9692ebe3-a676-45bb-a58d-b3fdbb1bbc2a">AuditSetSystemPolicy</a>
 

 

