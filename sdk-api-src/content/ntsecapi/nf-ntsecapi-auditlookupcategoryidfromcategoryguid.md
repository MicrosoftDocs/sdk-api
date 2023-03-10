---
UID: NF:ntsecapi.AuditLookupCategoryIdFromCategoryGuid
title: AuditLookupCategoryIdFromCategoryGuid function (ntsecapi.h)
description: Retrieves an element of the POLICY_AUDIT_EVENT_TYPE enumeration that represents the specified audit-policy category.
helpviewer_keywords: ["AuditLookupCategoryIdFromCategoryGuid","AuditLookupCategoryIdFromCategoryGuid function [Security]","ntsecapi/AuditLookupCategoryIdFromCategoryGuid","security.auditlookupcategoryidfromcategoryguid_func"]
old-location: security\auditlookupcategoryidfromcategoryguid_func.htm
tech.root: security
ms.assetid: c50e39f0-d45f-4deb-abe5-6261775b507c
ms.date: 12/05/2018
ms.keywords: AuditLookupCategoryIdFromCategoryGuid, AuditLookupCategoryIdFromCategoryGuid function [Security], ntsecapi/AuditLookupCategoryIdFromCategoryGuid, security.auditlookupcategoryidfromcategoryguid_func
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
 - AuditLookupCategoryIdFromCategoryGuid
 - ntsecapi/AuditLookupCategoryIdFromCategoryGuid
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
 - AuditLookupCategoryIdFromCategoryGuid
---

# AuditLookupCategoryIdFromCategoryGuid function


## -description

The <b>AuditLookupCategoryIdFromCategoryGuid</b> function retrieves an element of the <a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-policy_audit_event_type">POLICY_AUDIT_EVENT_TYPE</a> enumeration that represents the specified audit-policy category.

## -parameters

### -param pAuditCategoryGuid [in]

A pointer to a <b>GUID</b> structure that specifies an audit-policy category.

### -param pAuditCategoryId [out]

A pointer to an element of the <a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-policy_audit_event_type">POLICY_AUDIT_EVENT_TYPE</a> enumeration that represents the audit-policy category specified by the <i>pAuditCategoryGuid</i> parameter.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditlookupcategoryguidfromcategoryid">AuditLookupCategoryGuidFromCategoryId</a>