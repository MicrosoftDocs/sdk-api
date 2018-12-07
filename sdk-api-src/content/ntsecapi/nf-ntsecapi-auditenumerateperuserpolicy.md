---
UID: NF:ntsecapi.AuditEnumeratePerUserPolicy
title: AuditEnumeratePerUserPolicy function
author: windows-sdk-content
description: Enumerates users for whom per-user auditing policy is specified.
old-location: security\auditenumerateperuserpolicy_func.htm
tech.root: secauthz
ms.assetid: 4b13f021-ba08-4eb8-9c7a-0512992ef272
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AuditEnumeratePerUserPolicy, AuditEnumeratePerUserPolicy function [Security], ntsecapi/AuditEnumeratePerUserPolicy, security.auditenumerateperuserpolicy_func
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - API-MS-Win-Security-audit-l1-1-1.dll
 - sechost.dll
api_name:
 - AuditEnumeratePerUserPolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AuditEnumeratePerUserPolicy function


## -description


The <b>AuditEnumeratePerUserPolicy</b> function enumerates users for whom per-user auditing policy is specified. 


## -parameters




### -param ppAuditSidArray [out]

A pointer to a single buffer that contains both an array of pointers to <a href="https://msdn.microsoft.com/22f4255c-331a-4327-84d8-e905c7e419b6">POLICY_AUDIT_SID_ARRAY</a> structures and the structures themselves. The <b>POLICY_AUDIT_SID_ARRAY</b> structures specify the users for whom per-user audit policy is specified. 

When you have finished using this buffer, free it by calling the <a href="https://msdn.microsoft.com/697baf9b-91c4-4a88-a190-e9f6812e08af">AuditFree</a> function.


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



To successfully call this function, the caller must have <b>SeSecurityPrivilege</b> or have <b>AUDIT_ENUMERATE_USERS</b> access on the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Audit security object</a>.



