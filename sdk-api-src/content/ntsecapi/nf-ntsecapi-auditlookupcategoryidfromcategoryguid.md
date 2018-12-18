---
UID: NF:ntsecapi.AuditLookupCategoryIdFromCategoryGuid
title: AuditLookupCategoryIdFromCategoryGuid function
author: windows-sdk-content
description: Retrieves an element of the POLICY_AUDIT_EVENT_TYPE enumeration that represents the specified audit-policy category.
old-location: security\auditlookupcategoryidfromcategoryguid_func.htm
tech.root: secauthz
ms.assetid: c50e39f0-d45f-4deb-abe5-6261775b507c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AuditLookupCategoryIdFromCategoryGuid, AuditLookupCategoryIdFromCategoryGuid function [Security], ntsecapi/AuditLookupCategoryIdFromCategoryGuid, security.auditlookupcategoryidfromcategoryguid_func
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
 - AuditLookupCategoryIdFromCategoryGuid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AuditLookupCategoryIdFromCategoryGuid function


## -description


The <b>AuditLookupCategoryIdFromCategoryGuid</b> function retrieves an element of the <a href="https://msdn.microsoft.com/e8dbd1d5-37d5-4a97-9d1c-c645871dc7a5">POLICY_AUDIT_EVENT_TYPE</a> enumeration that represents the specified audit-policy category. 


## -parameters




### -param pAuditCategoryGuid [in]

A pointer to a <b>GUID</b> structure that specifies an audit-policy category.


### -param pAuditCategoryId [out]

A pointer to an element of the <a href="https://msdn.microsoft.com/e8dbd1d5-37d5-4a97-9d1c-c645871dc7a5">POLICY_AUDIT_EVENT_TYPE</a> enumeration that represents the audit-policy category specified by the <i>pAuditCategoryGuid</i> parameter.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/2f00fe52-2e94-473a-be13-252b50b58522">AuditLookupCategoryGuidFromCategoryId</a>
 

 

