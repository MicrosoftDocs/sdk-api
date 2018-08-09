---
UID: NF:ntsecapi.AuditLookupSubCategoryNameW
title: AuditLookupSubCategoryNameW function
author: windows-sdk-content
description: Retrieves the display name of the specified audit-policy subcategory.
old-location: security\auditlookupsubcategoryname_func.htm
old-project: secauthz
ms.assetid: 65ccd0f6-ee43-4b4d-98fd-b7a49f23ad9d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AuditLookupSubCategoryName, AuditLookupSubCategoryName function [Security], AuditLookupSubCategoryNameA, AuditLookupSubCategoryNameW, ntsecapi/AuditLookupSubCategoryName, ntsecapi/AuditLookupSubCategoryNameA, ntsecapi/AuditLookupSubCategoryNameW, security.auditlookupsubcategoryname_func
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
req.unicode-ansi: AuditLookupSubCategoryNameW (Unicode) and AuditLookupSubCategoryNameA (ANSI)
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
 - AuditLookupSubCategoryName
 - AuditLookupSubCategoryNameA
 - AuditLookupSubCategoryNameW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# AuditLookupSubCategoryNameW function


## -description


The <b>AuditLookupSubCategoryName</b> function retrieves the display name of the specified audit-policy subcategory. 


## -parameters




### -param pAuditSubCategoryGuid [in]

A pointer to a <b>GUID</b> structure that specifies an audit-policy subcategory.


### -param ppszSubCategoryName [out]

The address of a pointer to a null-terminated string that contains the display name of the audit-policy subcategory specified by the <i>pAuditSubCategoryGuid</i> parameter.

When you have finished using this string, free it by calling the <a href="https://msdn.microsoft.com/697baf9b-91c4-4a88-a190-e9f6812e08af">AuditFree</a> function.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/8b30d864-8eb5-42d8-bc9a-a9eae1de5187">AuditLookupCategoryName</a>
 

 

