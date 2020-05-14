---
UID: NS:ntdsapi.__unnamed_struct_2
title: DS_NAME_RESULT_ITEMW (ntdsapi.h)
description: The DS_NAME_RESULT_ITEM structure contains a name converted by the DsCrackNames function, along with associated error and domain data.helpviewer_keywords: ["*PDS_NAME_RESULT_ITEMW","DS_NAME_RESULT_ITEM","DS_NAME_RESULT_ITEM structure [Active Directory]","DS_NAME_RESULT_ITEMA","DS_NAME_RESULT_ITEMW","PDS_NAME_RESULT_ITEM","PDS_NAME_RESULT_ITEM structure pointer [Active Directory]","_glines_ds_name_result_item","ad.ds__name__result__item","ad.ds_name_result_item","ntdsapi/DS_NAME_RESULT_ITEM","ntdsapi/DS_NAME_RESULT_ITEMA","ntdsapi/DS_NAME_RESULT_ITEMW","ntdsapi/PDS_NAME_RESULT_ITEM"]
old-location: ad\ds_name_result_item.htm
tech.root: ad
ms.assetid: 50a4488f-e2d4-4671-b0e7-fb8cb4096c5c
ms.date: 12/05/2018
ms.keywords: '*PDS_NAME_RESULT_ITEMW, DS_NAME_RESULT_ITEM, DS_NAME_RESULT_ITEM structure [Active Directory], DS_NAME_RESULT_ITEMA, DS_NAME_RESULT_ITEMW, PDS_NAME_RESULT_ITEM, PDS_NAME_RESULT_ITEM structure pointer [Active Directory], _glines_ds_name_result_item, ad.ds__name__result__item, ad.ds_name_result_item, ntdsapi/DS_NAME_RESULT_ITEM, ntdsapi/DS_NAME_RESULT_ITEMA, ntdsapi/DS_NAME_RESULT_ITEMW, ntdsapi/PDS_NAME_RESULT_ITEM'
f1_keywords:
- ntdsapi/DS_NAME_RESULT_ITEM
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: DS_NAME_RESULT_ITEMW, *PDS_NAME_RESULT_ITEMW
req.redist: 
ms.custom: 19H1
---

# DS_NAME_RESULT_ITEMW structure


## -description


The <b>DS_NAME_RESULT_ITEM</b> structure contains a name converted by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a> function, along with associated error and domain data.


## -struct-fields




### -field status

Contains one of the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_name_error">DS_NAME_ERROR</a> values that indicates the status of this name conversion.


### -field string

 


### -field unique

 


### -field pDomain

Pointer to a null-terminated string that specifies the DNS domain in which the object resides. This member will contain valid data if <b>status</b> contains <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_name_error">DS_NAME_NO_ERROR</a> or <b>DS_NAME_ERROR_DOMAIN_ONLY</b>.


### -field pName

Pointer to a null-terminated string that specifies the newly formatted object name.


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a> function returns an array of <b>DS_NAME_RESULT_ITEM</b> structures as part of the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/domain-controller-and-replication-management-structures">Domain Controller and Replication Management Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a>
 

 

