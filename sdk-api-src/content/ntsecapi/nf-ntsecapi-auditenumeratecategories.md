---
UID: NF:ntsecapi.AuditEnumerateCategories
title: AuditEnumerateCategories function (ntsecapi.h)
description: Enumerates the available audit-policy categories.
helpviewer_keywords: ["AuditEnumerateCategories","AuditEnumerateCategories function [Security]","ntsecapi/AuditEnumerateCategories","security.auditenumeratecategories_func"]
old-location: security\auditenumeratecategories_func.htm
tech.root: security
ms.assetid: bcfdb24b-182e-4845-95c0-a210915435ae
ms.date: 12/05/2018
ms.keywords: AuditEnumerateCategories, AuditEnumerateCategories function [Security], ntsecapi/AuditEnumerateCategories, security.auditenumeratecategories_func
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AuditEnumerateCategories
 - ntsecapi/AuditEnumerateCategories
dev_langs:
 - c++
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
 - AuditEnumerateCategories
---

# AuditEnumerateCategories function


## -description

The <b>AuditEnumerateCategories</b> function enumerates the available audit-policy categories.

## -parameters

### -param ppAuditCategoriesArray [out]

A pointer to a single buffer that contains both an array of pointers to <b>GUID</b> structures and the structures themselves. The <b>GUID</b> structures specify the audit-policy categories available on the computer. 

When you have finished using this buffer, free it by calling the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditfree">AuditFree</a> function.

### -param pdwCountReturned [out]

A pointer to the number of elements in the <i>ppAuditCategoriesArray</i> array.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditenumeratesubcategories">AuditEnumerateSubCategories</a>