---
UID: NF:ntsecapi.AuditLookupSubCategoryNameW
title: AuditLookupSubCategoryNameW function (ntsecapi.h)
description: Retrieves the display name of the specified audit-policy subcategory. (Unicode)
helpviewer_keywords: ["AuditLookupSubCategoryName", "AuditLookupSubCategoryName function [Security]", "AuditLookupSubCategoryNameW", "ntsecapi/AuditLookupSubCategoryName", "ntsecapi/AuditLookupSubCategoryNameW", "security.auditlookupsubcategoryname_func"]
old-location: security\auditlookupsubcategoryname_func.htm
tech.root: security
ms.assetid: 65ccd0f6-ee43-4b4d-98fd-b7a49f23ad9d
ms.date: 12/05/2018
ms.keywords: AuditLookupSubCategoryName, AuditLookupSubCategoryName function [Security], AuditLookupSubCategoryNameA, AuditLookupSubCategoryNameW, ntsecapi/AuditLookupSubCategoryName, ntsecapi/AuditLookupSubCategoryNameA, ntsecapi/AuditLookupSubCategoryNameW, security.auditlookupsubcategoryname_func
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AuditLookupSubCategoryNameW
 - ntsecapi/AuditLookupSubCategoryNameW
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
 - AuditLookupSubCategoryName
 - AuditLookupSubCategoryNameA
 - AuditLookupSubCategoryNameW
---

# AuditLookupSubCategoryNameW function


## -description

The <b>AuditLookupSubCategoryName</b> function retrieves the display name of the specified audit-policy subcategory.

## -parameters

### -param pAuditSubCategoryGuid [in]

A pointer to a <b>GUID</b> structure that specifies an audit-policy subcategory.

### -param ppszSubCategoryName [out]

The address of a pointer to a null-terminated string that contains the display name of the audit-policy subcategory specified by the <i>pAuditSubCategoryGuid</i> parameter.

When you have finished using this string, free it by calling the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditfree">AuditFree</a> function.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditlookupcategorynamea">AuditLookupCategoryName</a>

## -remarks

> [!NOTE]
> The ntsecapi.h header defines AuditLookupSubCategoryName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
