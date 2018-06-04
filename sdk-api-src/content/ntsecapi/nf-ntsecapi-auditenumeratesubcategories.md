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

When you have finished using this buffer, free it by calling the <a href="https://msdn.microsoft.com/697baf9b-91c4-4a88-a190-e9f6812e08af">AuditFree</a> function.


### -param pdwCountReturned

TBD




#### - pCountReturned [out]

A pointer to the number of audit-policy subcategories returned in the <i>ppAuditSubCategoriesArray</i> array.


## -returns




						If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/bcfdb24b-182e-4845-95c0-a210915435ae">AuditEnumerateCategories</a>
 

 

