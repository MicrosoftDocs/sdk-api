---
UID: NS:ntdsapi.DS_NAME_RESULT_ITEMA
title: DS_NAME_RESULT_ITEMA (ntdsapi.h)
description: The DS_NAME_RESULT_ITEM structure contains a name converted by the DsCrackNames function, along with associated error and domain data. (ANSI)
helpviewer_keywords: ["*PDS_NAME_RESULT_ITEMA","DS_NAME_RESULT_ITEM","DS_NAME_RESULT_ITEM structure [Active Directory]","DS_NAME_RESULT_ITEMA","DS_NAME_RESULT_ITEMW","PDS_NAME_RESULT_ITEM","PDS_NAME_RESULT_ITEM structure pointer [Active Directory]","_glines_ds_name_result_item","ad.ds__name__result__item","ad.ds_name_result_item","ntdsapi/DS_NAME_RESULT_ITEM","ntdsapi/DS_NAME_RESULT_ITEMA","ntdsapi/DS_NAME_RESULT_ITEMW","ntdsapi/PDS_NAME_RESULT_ITEM"]
old-location: ad\ds_name_result_item.htm
tech.root: ad
ms.assetid: 50a4488f-e2d4-4671-b0e7-fb8cb4096c5c
ms.date: 12/05/2018
ms.keywords: '*PDS_NAME_RESULT_ITEMA, DS_NAME_RESULT_ITEM, DS_NAME_RESULT_ITEM structure [Active Directory], DS_NAME_RESULT_ITEMA, DS_NAME_RESULT_ITEMW, PDS_NAME_RESULT_ITEM, PDS_NAME_RESULT_ITEM structure pointer [Active Directory], _glines_ds_name_result_item, ad.ds__name__result__item, ad.ds_name_result_item, ntdsapi/DS_NAME_RESULT_ITEM, ntdsapi/DS_NAME_RESULT_ITEMA, ntdsapi/DS_NAME_RESULT_ITEMW, ntdsapi/PDS_NAME_RESULT_ITEM'
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
targetos: Windows
req.typenames: DS_NAME_RESULT_ITEMA, *PDS_NAME_RESULT_ITEMA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDS_NAME_RESULT_ITEMA
 - ntdsapi/PDS_NAME_RESULT_ITEMA
 - DS_NAME_RESULT_ITEMA
 - ntdsapi/DS_NAME_RESULT_ITEMA
dev_langs:
 - c++
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
---

# DS_NAME_RESULT_ITEMA structure


## -description

The <b>DS_NAME_RESULT_ITEM</b> structure contains a name converted by the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a> function, along with associated error and domain data.

## -struct-fields

### -field status

Contains one of the <a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_name_error">DS_NAME_ERROR</a> values that indicates the status of this name conversion.

### -field string

### -field unique

### -field pDomain

Pointer to a null-terminated string that specifies the DNS domain in which the object resides. This member will contain valid data if <b>status</b> contains <a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_name_error">DS_NAME_NO_ERROR</a> or <b>DS_NAME_ERROR_DOMAIN_ONLY</b>.

### -field pName

Pointer to a null-terminated string that specifies the newly formatted object name.

## -remarks

The <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a> function returns an array of <b>DS_NAME_RESULT_ITEM</b> structures as part of the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure.





> [!NOTE]
> The ntdsapi.h header defines DS_NAME_RESULT_ITEM as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a>



<a href="/windows/desktop/AD/domain-controller-and-replication-management-structures">Domain Controller and Replication Management Structures</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a>

