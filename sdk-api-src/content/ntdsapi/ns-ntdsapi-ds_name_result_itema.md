---
UID: NS:ntdsapi.DS_NAME_RESULT_ITEMA
title: DS_NAME_RESULT_ITEMA
author: windows-sdk-content
description: The DS_NAME_RESULT_ITEM structure contains a name converted by the DsCrackNames function, along with associated error and domain data.
old-location: ad\ds_name_result_item.htm
old-project: AD
ms.assetid: 50a4488f-e2d4-4671-b0e7-fb8cb4096c5c
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*PDS_NAME_RESULT_ITEMA, DS_NAME_RESULT_ITEM, DS_NAME_RESULT_ITEM structure [Active Directory], DS_NAME_RESULT_ITEMA, DS_NAME_RESULT_ITEMW, PDS_NAME_RESULT_ITEM, PDS_NAME_RESULT_ITEM structure pointer [Active Directory], _glines_ds_name_result_item, ad.ds__name__result__item, ad.ds_name_result_item, ntdsapi/DS_NAME_RESULT_ITEM, ntdsapi/DS_NAME_RESULT_ITEMA, ntdsapi/DS_NAME_RESULT_ITEMW, ntdsapi/PDS_NAME_RESULT_ITEM"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DS_NAME_RESULT_ITEMW (Unicode) and DS_NAME_RESULT_ITEMA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DS_NAME_RESULT_ITEMA, *PDS_NAME_RESULT_ITEMA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_NAME_RESULT_ITEM
 - DS_NAME_RESULT_ITEMA
 - DS_NAME_RESULT_ITEMW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# DS_NAME_RESULT_ITEMA structure


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
 

 

