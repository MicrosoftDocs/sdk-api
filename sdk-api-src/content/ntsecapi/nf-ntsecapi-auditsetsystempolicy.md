---
UID: NF:ntsecapi.AuditSetSystemPolicy
title: AuditSetSystemPolicy function (ntsecapi.h)
author: windows-sdk-content
description: Sets system audit policy for one or more audit-policy subcategories.
old-location: security\auditsetsystempolicy_func.htm
tech.root: SecAuthZ
ms.assetid: 9692ebe3-a676-45bb-a58d-b3fdbb1bbc2a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AuditSetSystemPolicy, AuditSetSystemPolicy function [Security], ntsecapi/AuditSetSystemPolicy, security.auditsetsystempolicy_func
ms.topic: function
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - API-MS-Win-Security-audit-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-audit-l1-1-1.dll
api_name:
 - AuditSetSystemPolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AuditSetSystemPolicy function


## -description


The <b>AuditSetSystemPolicy</b> function sets system audit policy for one or more audit-policy subcategories. 


## -parameters




### -param pAuditPolicy [in]

A pointer to an array of <a href="https://msdn.microsoft.com/3fafeec9-a028-4a65-933e-fb973eb257b0">AUDIT_POLICY_INFORMATION</a> structures. Each structure specifies system audit policy for one audit-policy subcategory.

The <b>AuditCategoryGuid</b> member of these structures is ignored.


### -param dwPolicyCount [in]

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
</table>
 




## -remarks



To successfully call this function, the caller must have <b>SeSecurityPrivilege</b> or have <b>AUDIT_SET_SYSTEM_POLICY</b> access on the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Audit security object</a>.




## -see-also




<a href="https://msdn.microsoft.com/7d4790de-ebd6-4840-b532-7158b8d80db2">AuditQueryPerUserPolicy</a>



<a href="https://msdn.microsoft.com/5c268033-65fd-4a74-90a1-4b9e1e18daf1">AuditQuerySystemPolicy</a>



<a href="https://msdn.microsoft.com/a6cef640-5658-4c13-96fb-a664d2a61b57">AuditSetPerUserPolicy</a>
 

 

