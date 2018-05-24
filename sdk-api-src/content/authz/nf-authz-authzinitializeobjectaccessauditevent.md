---
UID: NF:authz.AuthzInitializeObjectAccessAuditEvent
title: AuthzInitializeObjectAccessAuditEvent function
author: windows-driver-content
description: Initializes auditing for an object.
old-location: security\authzinitializeobjectaccessauditevent.htm
old-project: SecAuthZ
ms.assetid: cf79a92f-31e0-47cf-8990-4dbd46056a90
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: AUTHZ_NO_ALLOC_STRINGS, AUTHZ_NO_FAILURE_AUDIT, AUTHZ_NO_SUCCESS_AUDIT, AuthzInitializeObjectAccessAuditEvent, AuthzInitializeObjectAccessAuditEvent function [Security], _win32_authzinitializeobjectaccessauditevent, authz/AuthzInitializeObjectAccessAuditEvent, security.authzinitializeobjectaccessauditevent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: authz.h
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
req.typenames: AUTHZ_CONTEXT_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Authz.dll
api_name:
-	AuthzInitializeObjectAccessAuditEvent
product: Windows
targetos: Windows
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
---

# AuthzInitializeObjectAccessAuditEvent function


## -description


The <b>AuthzInitializeObjectAccessAuditEvent</b> function initializes auditing for an object.


## -parameters




### -param Flags [in]

Modifies the audit. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_NO_SUCCESS_AUDIT"></a><a id="authz_no_success_audit"></a><dl>
<dt><b>AUTHZ_NO_SUCCESS_AUDIT</b></dt>
</dl>
</td>
<td width="60%">
Disable generation of success audits.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_NO_FAILURE_AUDIT"></a><a id="authz_no_failure_audit"></a><dl>
<dt><b>AUTHZ_NO_FAILURE_AUDIT</b></dt>
</dl>
</td>
<td width="60%">
Disable generation of failure audits.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_NO_ALLOC_STRINGS"></a><a id="authz_no_alloc_strings"></a><dl>
<dt><b>AUTHZ_NO_ALLOC_STRINGS</b></dt>
</dl>
</td>
<td width="60%">
Use pointers to the passed strings instead of allocating memory and copying the strings. The calling application must ensure that the passed memory stays valid during access checks.

</td>
</tr>
</table>
 


### -param hAuditEventType [in]

Reserved. This parameter should be set to <b>NULL</b>. 

					


### -param szOperationType [in]

String that indicates the operation that is to be audited. 

					


### -param szObjectType [in]

String that indicates the type of object being accessed. 

					


### -param szObjectName [in]

String the indicates the name of the object being accessed. 

					


### -param szAdditionalInfo [in]


					String, defined by the Resource Manager, for additional audit information. 



### -param phAuditEvent [out]

Pointer that receives an <b>AUTHZ_AUDIT_EVENT_HANDLE</b> structure. 

					


### -param dwAdditionalParameterCount

TBD


### -param param

TBD




#### - dwAdditionalParamCount [in]

Must be set to zero. 

					


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>
 

 

