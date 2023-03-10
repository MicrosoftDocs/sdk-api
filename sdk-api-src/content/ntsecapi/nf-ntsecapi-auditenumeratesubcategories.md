---
UID: NF:ntsecapi.AuditEnumerateSubCategories
title: AuditEnumerateSubCategories function (ntsecapi.h)
description: Enumerates the available audit-policy subcategories.
helpviewer_keywords: ["AuditEnumerateSubCategories","AuditEnumerateSubCategories function [Security]","ntsecapi/AuditEnumerateSubCategories","security.auditenumeratesubcategories_func"]
old-location: security\auditenumeratesubcategories_func.htm
tech.root: security
ms.assetid: c5af83f4-9524-4a39-ad1d-39b21bb073bd
ms.date: 12/05/2018
ms.keywords: AuditEnumerateSubCategories, AuditEnumerateSubCategories function [Security], ntsecapi/AuditEnumerateSubCategories, security.auditenumeratesubcategories_func
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
 - AuditEnumerateSubCategories
 - ntsecapi/AuditEnumerateSubCategories
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
 - AuditEnumerateSubCategories
---

# AuditEnumerateSubCategories function


## -description

The <b>AuditEnumerateSubCategories</b> function enumerates the available audit-policy subcategories.

## -parameters

### -param pAuditCategoryGuid [in]

The <b>GUID</b> of an audit-policy category for which subcategories are enumerated. If the value of the <i>bRetrieveAllSubCategories</i> parameter is <b>TRUE</b>, this parameter is ignored.

### -param bRetrieveAllSubCategories [in]

<b>TRUE</b> to enumerate all audit-policy subcategories; <b>FALSE</b> to enumerate only the subcategories of the audit-policy category specified by the <i>pAuditCategoryGuid</i> parameter.

### -param ppAuditSubCategoriesArray [out]

A pointer to a single buffer that contains both an array of pointers to <b>GUID</b> structures and the structures themselves. The <b>GUID</b> structures specify the audit-policy subcategories available on the computer. 

When you have finished using this buffer, free it by calling the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditfree">AuditFree</a> function.

### -param pdwCountReturned [out]

A pointer to the number of audit-policy subcategories returned in the <i>ppAuditSubCategoriesArray</i> array.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditenumeratecategories">AuditEnumerateCategories</a>