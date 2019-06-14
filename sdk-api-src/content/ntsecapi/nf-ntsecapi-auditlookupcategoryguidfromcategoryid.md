---
UID: NF:ntsecapi.AuditLookupCategoryGuidFromCategoryId
title: AuditLookupCategoryGuidFromCategoryId function (ntsecapi.h)
author: windows-sdk-content
description: Retrieves a GUID structure that represents the specified audit-policy category.
old-location: security\auditlookupcategoryguidfromcategoryid_func.htm
tech.root: SecAuthZ
ms.assetid: 2f00fe52-2e94-473a-be13-252b50b58522
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AuditLookupCategoryGuidFromCategoryId, AuditLookupCategoryGuidFromCategoryId function [Security], ntsecapi/AuditLookupCategoryGuidFromCategoryId, security.auditlookupcategoryguidfromcategoryid_func
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - AuditLookupCategoryGuidFromCategoryId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AuditLookupCategoryGuidFromCategoryId function


## -description


The <b>AuditLookupCategoryGuidFromCategoryId</b> function retrieves a <b>GUID</b> structure that represents the specified audit-policy category. 


## -parameters




### -param AuditCategoryId [in]

An element of the <a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/ne-ntsecapi-_policy_audit_event_type">POLICY_AUDIT_EVENT_TYPE</a> enumeration that specifies an audit-policy category.


### -param pAuditCategoryGuid [out]

A pointer to a <b>GUID</b> structure that represents the audit-policy category specified by the  <i>AuditCategoryId</i>


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-auditlookupcategoryidfromcategoryguid">AuditLookupCategoryIdFromCategoryGuid</a>
 

 

