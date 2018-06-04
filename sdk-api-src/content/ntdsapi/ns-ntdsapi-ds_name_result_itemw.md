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

# DS_NAME_RESULT_ITEMW structure


## -description


The <b>DS_NAME_RESULT_ITEM</b> structure contains a name converted by the 
<a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a> function, along with associated error and domain data.


## -struct-fields




### -field status

Contains one of the <a href="https://msdn.microsoft.com/8475133c-4bc8-4545-bd54-15d4e7b07869">DS_NAME_ERROR</a> values that indicates the status of this name conversion.


### -field pDomain.string

 


### -field pDomain.unique

 


### -field pName.string

 


### -field pName.unique

 


### -field pDomain

Pointer to a null-terminated string that specifies the DNS domain in which the object resides. This member will contain valid data if <b>status</b> contains <a href="https://msdn.microsoft.com/8475133c-4bc8-4545-bd54-15d4e7b07869">DS_NAME_NO_ERROR</a> or <b>DS_NAME_ERROR_DOMAIN_ONLY</b>.


### -field pName

Pointer to a null-terminated string that specifies the newly formatted object name.


## -remarks



The <a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a> function returns an array of <b>DS_NAME_RESULT_ITEM</b> structures as part of the <a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a>



<a href="https://msdn.microsoft.com/42b20d3b-1799-4f5f-b74e-fe9284dd8ac3">Domain Controller and Replication Management Structures</a>



<a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a>
 

 

