---
UID: NF:ntsecapi.AuditLookupCategoryGuidFromCategoryId
title: AuditLookupCategoryGuidFromCategoryId function
author: windows-sdk-content
description: Retrieves a GUID structure that represents the specified audit-policy category.
old-location: security\auditlookupcategoryguidfromcategoryid_func.htm
old-project: SecAuthZ
ms.assetid: 2f00fe52-2e94-473a-be13-252b50b58522
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AuditLookupCategoryGuidFromCategoryId, AuditLookupCategoryGuidFromCategoryId function [Security], ntsecapi/AuditLookupCategoryGuidFromCategoryId, security.auditlookupcategoryguidfromcategoryid_func
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntsecapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# AuditLookupCategoryGuidFromCategoryId function


## -description


The <b>AuditLookupCategoryGuidFromCategoryId</b> function retrieves a <b>GUID</b> structure that represents the specified audit-policy category. 


## -parameters




### -param AuditCategoryId [in]

An element of the <a href="https://msdn.microsoft.com/e8dbd1d5-37d5-4a97-9d1c-c645871dc7a5">POLICY_AUDIT_EVENT_TYPE</a> enumeration that specifies an audit-policy category.


### -param pAuditCategoryGuid [out]

A pointer to a <b>GUID</b> structure that represents the audit-policy category specified by the  <i>AuditCategoryId</i>


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/c50e39f0-d45f-4deb-abe5-6261775b507c">AuditLookupCategoryIdFromCategoryGuid</a>
 

 

