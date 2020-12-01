---
UID: NF:ntsecapi.AuditLookupCategoryGuidFromCategoryId
title: AuditLookupCategoryGuidFromCategoryId function (ntsecapi.h)
description: Retrieves a GUID structure that represents the specified audit-policy category.
helpviewer_keywords: ["AuditLookupCategoryGuidFromCategoryId","AuditLookupCategoryGuidFromCategoryId function [Security]","ntsecapi/AuditLookupCategoryGuidFromCategoryId","security.auditlookupcategoryguidfromcategoryid_func"]
old-location: security\auditlookupcategoryguidfromcategoryid_func.htm
tech.root: security
ms.assetid: 2f00fe52-2e94-473a-be13-252b50b58522
ms.date: 12/05/2018
ms.keywords: AuditLookupCategoryGuidFromCategoryId, AuditLookupCategoryGuidFromCategoryId function [Security], ntsecapi/AuditLookupCategoryGuidFromCategoryId, security.auditlookupcategoryguidfromcategoryid_func
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
 - AuditLookupCategoryGuidFromCategoryId
 - ntsecapi/AuditLookupCategoryGuidFromCategoryId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - AuditLookupCategoryGuidFromCategoryId
---

# AuditLookupCategoryGuidFromCategoryId function


## -description

The <b>AuditLookupCategoryGuidFromCategoryId</b> function retrieves a <b>GUID</b> structure that represents the specified audit-policy category.

## -parameters

### -param AuditCategoryId [in]

An element of the <a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-policy_audit_event_type">POLICY_AUDIT_EVENT_TYPE</a> enumeration that specifies an audit-policy category.

### -param pAuditCategoryGuid [out]

A pointer to a <b>GUID</b> structure that represents the audit-policy category specified by the  <i>AuditCategoryId</i>

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditlookupcategoryidfromcategoryguid">AuditLookupCategoryIdFromCategoryGuid</a>