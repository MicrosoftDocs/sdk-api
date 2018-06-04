---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# AuditLookupSubCategoryNameW function


## -description


The <b>AuditLookupSubCategoryName</b> function retrieves the display name of the specified audit-policy subcategory. 


## -parameters




### -param pAuditSubCategoryGuid [in]

A pointer to a <b>GUID</b> structure that specifies an audit-policy subcategory.


### -param ppszSubCategoryName [out]

The address of a pointer to a null-terminated string that contains the display name of the audit-policy subcategory specified by the <i>pAuditSubCategoryGuid</i> parameter.

When you have finished using this string, free it by calling the <a href="https://msdn.microsoft.com/697baf9b-91c4-4a88-a190-e9f6812e08af">AuditFree</a> function.


## -returns




						If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/8b30d864-8eb5-42d8-bc9a-a9eae1de5187">AuditLookupCategoryName</a>
 

 

