---
UID: NF:ntsecapi.AuditLookupCategoryNameW
title: AuditLookupCategoryNameW function (ntsecapi.h)
description: Retrieves the display name of the specified audit-policy category.helpviewer_keywords: ["AuditLookupCategoryName","AuditLookupCategoryName function [Security]","AuditLookupCategoryNameA","AuditLookupCategoryNameW","ntsecapi/AuditLookupCategoryName","ntsecapi/AuditLookupCategoryNameA","ntsecapi/AuditLookupCategoryNameW","security.auditlookupcategoryname_func"]
old-location: security\auditlookupcategoryname_func.htm
tech.root: SecAuthZ
ms.assetid: 8b30d864-8eb5-42d8-bc9a-a9eae1de5187
ms.date: 12/05/2018
ms.keywords: AuditLookupCategoryName, AuditLookupCategoryName function [Security], AuditLookupCategoryNameA, AuditLookupCategoryNameW, ntsecapi/AuditLookupCategoryName, ntsecapi/AuditLookupCategoryNameA, ntsecapi/AuditLookupCategoryNameW, security.auditlookupcategoryname_func
f1_keywords:
- ntsecapi/AuditLookupCategoryName
dev_langs:
- c++
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
- AuditLookupCategoryName
- AuditLookupCategoryNameA
- AuditLookupCategoryNameW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AuditLookupCategoryNameW function


## -description


The <b>AuditLookupCategoryName</b> function retrieves the display name of the specified audit-policy category. 


## -parameters




### -param pAuditCategoryGuid [in]

A pointer to a <b>GUID</b> structure that specifies an audit-policy category.


### -param ppszCategoryName [out]

The address of a pointer to a null-terminated string that contains the display name of the audit-policy category specified by the <i>pAuditCategoryGuid</i> function.

When you have finished using this string, free it by calling the <a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-auditfree">AuditFree</a> function.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-auditlookupsubcategorynamea">AuditLookupSubCategoryName</a>
 

 

