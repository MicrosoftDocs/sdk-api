---
UID: NF:authz.AuthzFreeAuditEvent
title: AuthzFreeAuditEvent function
author: windows-sdk-content
description: Frees the structure allocated by the AuthzInitializeObjectAccessAuditEvent function.
old-location: security\authzfreeauditevent.htm
tech.root: secauthz
ms.assetid: e2980ef7-45dd-47c7-ba4d-f36b52bbd7dc
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: AuthzFreeAuditEvent, AuthzFreeAuditEvent function [Security], _win32_authzfreeauditevent, authz/AuthzFreeAuditEvent, security.authzfreeauditevent
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
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
 - Ext-MS-Win-authz-context-l1-1-0.dll
api_name:
 - AuthzFreeAuditEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
- apiref
: 
- 
: 
- AuthzFreeAuditEvent
: 
---

# AuthzFreeAuditEvent function


## -description


The <b>AuthzFreeAuditEvent</b> function frees the  structure allocated by the 
<a href="https://msdn.microsoft.com/cf79a92f-31e0-47cf-8990-4dbd46056a90">AuthzInitializeObjectAccessAuditEvent</a> function.


## -parameters




### -param hAuditEvent [in]

A pointer to the <b>AUTHZ_AUDIT_EVENT_HANDLE</b> structure to be freed.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/cf79a92f-31e0-47cf-8990-4dbd46056a90">AuthzInitializeObjectAccessAuditEvent</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>
 

 

