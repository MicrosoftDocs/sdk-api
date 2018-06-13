---
UID: NF:authz.AuthzOpenObjectAudit
title: AuthzOpenObjectAudit function
author: windows-sdk-content
description: Reads the system access control list (SACL) of the specified security descriptor and generates any appropriate audits specified by that SACL.
old-location: security\authzopenobjectaudit.htm
old-project: SecAuthZ
ms.assetid: 39c6f0bc-72bf-4a82-b417-c0c5b2626344
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AuthzOpenObjectAudit, AuthzOpenObjectAudit function [Security], _win32_authzopenobjectaudit, authz/AuthzOpenObjectAudit, security.authzopenobjectaudit
ms.prod: windows
ms.technology: windows-sdk
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
 - AuthzOpenObjectAudit
product: Windows
targetos: Windows
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
---

# AuthzOpenObjectAudit function


## -description


The <b>AuthzOpenObjectAudit</b> function reads the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) of the specified security descriptor and generates any appropriate audits specified by that SACL.


## -parameters




### -param Flags [in]

Reserved for future use.


### -param hAuthzClientContext [in]

A handle to the client context of the object to open.


### -param pRequest [in]

A pointer to an 
<a href="https://msdn.microsoft.com/3748075c-b31a-4669-b8a6-1a540449d8fa">AUTHZ_ACCESS_REQUEST</a> structure.


### -param hAuditEvent [in]

A handle to the audit event to use.


### -param pSecurityDescriptor [in]

A pointer to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure for the object.


### -param OPTIONAL

TBD


### -param OptionalSecurityDescriptorCount

TBD


### -param pReply [in]

A pointer to an 
<a href="https://msdn.microsoft.com/7162bf80-3730-46d7-a603-2a55b969c9ba">AUTHZ_ACCESS_REPLY</a> structure.


#### - SecurityDescriptorArray [in]

A pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structures.


#### - SecurityDescriptorCount [in]

The number of elements in <i>SecurityDescriptorArray</i>. 

					


## -returns



If the function succeeds, it returns a nonzero value. 

If the function fails, it returns a zero value. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://www.bing.com/search?q=Basic+Access+Control+Functions">Basic Access Control Functions</a>
 

 

