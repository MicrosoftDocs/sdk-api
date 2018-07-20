---
UID: NF:ntsecapi.AuditLookupCategoryNameA
title: AuditLookupCategoryNameA function
author: windows-sdk-content
description: Retrieves the display name of the specified audit-policy category.
old-location: security\auditlookupcategoryname_func.htm
old-project: SecAuthZ
ms.assetid: 8b30d864-8eb5-42d8-bc9a-a9eae1de5187
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: AuditLookupCategoryName, AuditLookupCategoryName function [Security], AuditLookupCategoryNameA, AuditLookupCategoryNameW, ntsecapi/AuditLookupCategoryName, ntsecapi/AuditLookupCategoryNameA, ntsecapi/AuditLookupCategoryNameW, security.auditlookupcategoryname_func
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AuditLookupCategoryNameW (Unicode) and AuditLookupCategoryNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
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
 - AuditLookupCategoryName
 - AuditLookupCategoryNameA
 - AuditLookupCategoryNameW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# AuditLookupCategoryNameA function


## -description


The <b>AuditLookupCategoryName</b> function retrieves the display name of the specified audit-policy category. 


## -parameters




### -param pAuditCategoryGuid [in]

A pointer to a <b>GUID</b> structure that specifies an audit-policy category.


### -param ppszCategoryName [out]

The address of a pointer to a null-terminated string that contains the display name of the audit-policy category specified by the <i>pAuditCategoryGuid</i> function.

When you have finished using this string, free it by calling the <a href="https://msdn.microsoft.com/697baf9b-91c4-4a88-a190-e9f6812e08af">AuditFree</a> function.


## -returns




						If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/65ccd0f6-ee43-4b4d-98fd-b7a49f23ad9d">AuditLookupSubCategoryName</a>
 

 

