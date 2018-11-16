---
UID: NF:ntsecapi.AuditEnumerateCategories
title: AuditEnumerateCategories function
author: windows-sdk-content
description: Enumerates the available audit-policy categories.
old-location: security\auditenumeratecategories_func.htm
tech.root: SecAuthZ
ms.assetid: bcfdb24b-182e-4845-95c0-a210915435ae
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AuditEnumerateCategories, AuditEnumerateCategories function [Security], ntsecapi/AuditEnumerateCategories, security.auditenumeratecategories_func
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - API-MS-Win-Security-audit-l1-1-1.dll
 - sechost.dll
api_name:
 - AuditEnumerateCategories
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- AuditEnumerateCategories
: 
---

# AuditEnumerateCategories function


## -description


The <b>AuditEnumerateCategories</b> function enumerates the available audit-policy categories. 


## -parameters




### -param ppAuditCategoriesArray [out]

A pointer to a single buffer that contains both an array of pointers to <b>GUID</b> structures and the structures themselves. The <b>GUID</b> structures specify the audit-policy categories available on the computer. 

When you have finished using this buffer, free it by calling the <a href="https://msdn.microsoft.com/697baf9b-91c4-4a88-a190-e9f6812e08af">AuditFree</a> function.


### -param pdwCountReturned [out]

A pointer to the number of elements in the <i>ppAuditCategoriesArray</i> array.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/c5af83f4-9524-4a39-ad1d-39b21bb073bd">AuditEnumerateSubCategories</a>
 

 

