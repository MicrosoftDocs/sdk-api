---
UID: NF:authz.AuthzInitializeObjectAccessAuditEvent2
title: AuthzInitializeObjectAccessAuditEvent2 function
author: windows-sdk-content
description: Allocates and initializes an AUTHZ_AUDIT_EVENT_HANDLE handle for use with the AuthzAccessCheck function.
old-location: security\authzinitializeobjectaccessauditevent2.htm
old-project: secauthz
ms.assetid: c65bb799-0158-496a-b428-0331c4474b74
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AUTHZ_NO_ALLOC_STRINGS, AUTHZ_NO_FAILURE_AUDIT, AUTHZ_NO_SUCCESS_AUDIT, AuthzInitializeObjectAccessAuditEvent2, AuthzInitializeObjectAccessAuditEvent2 function [Security], authz/AuthzInitializeObjectAccessAuditEvent2, security.authzinitializeobjectaccessauditevent2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: authz.h
req.include-header: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: AUTHZ_CONTEXT_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzInitializeObjectAccessAuditEvent2
product: Windows
targetos: Windows
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
---

# AuthzInitializeObjectAccessAuditEvent2 function


## -description


The <b>AuthzInitializeObjectAccessAuditEvent2</b> function allocates and initializes an <b>AUTHZ_AUDIT_EVENT_HANDLE</b> handle for use with the <a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> function.


## -parameters




### -param Flags [in]

Flags that modify the behavior of the audit. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_NO_ALLOC_STRINGS"></a><a id="authz_no_alloc_strings"></a><dl>
<dt><b>AUTHZ_NO_ALLOC_STRINGS</b></dt>
</dl>
</td>
<td width="60%">
Uses pointers to the passed strings instead of allocating memory and copying the strings. The calling application must ensure that the passed memory remains valid during access checks.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_NO_FAILURE_AUDIT"></a><a id="authz_no_failure_audit"></a><dl>
<dt><b>AUTHZ_NO_FAILURE_AUDIT</b></dt>
</dl>
</td>
<td width="60%">
Disables generation of failure audits.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_NO_SUCCESS_AUDIT"></a><a id="authz_no_success_audit"></a><dl>
<dt><b>AUTHZ_NO_SUCCESS_AUDIT</b></dt>
</dl>
</td>
<td width="60%">
Disables generation of success audits.

</td>
</tr>
</table>
 


### -param hAuditEventType [in]

Reserved. This parameter should be set to <b>NULL</b>.


### -param szOperationType [in]

A pointer to a string that indicates the operation that is to be audited.


### -param szObjectType [in]

A pointer to a string that indicates the type of object  accessed.


### -param szObjectName [in]

A pointer to a string that indicates the name of the object  accessed.


### -param szAdditionalInfo [in]

Pointer to a string defined by the Resource Manager that contains additional audit information.


### -param szAdditionalInfo2 [in]

Pointer to a string defined by the Resource Manager that contains additional audit information.


### -param phAuditEvent [out]

A pointer to the returned <b>AUTHZ_AUDIT_EVENT_HANDLE</b> handle.


### -param dwAdditionalParameterCount [in]

Must be set to zero.


### -param param

TBD




## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>
 

 

