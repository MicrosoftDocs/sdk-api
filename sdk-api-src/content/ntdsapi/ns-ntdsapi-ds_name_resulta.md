---
UID: NS:ntdsapi.DS_NAME_RESULTA
title: DS_NAME_RESULTA (ntdsapi.h)
description: The DS_NAME_RESULT structure is used with the DsCrackNames function to contain the names converted by the function. (ANSI)
helpviewer_keywords: ["*PDS_NAME_RESULTA","DS_NAME_RESULT","DS_NAME_RESULT structure [Active Directory]","DS_NAME_RESULTA","DS_NAME_RESULTW","PDS_NAME_RESULT","PDS_NAME_RESULT structure pointer [Active Directory]","_glines_ds_name_result","ad.ds__name__result","ad.ds_name_result","ntdsapi/DS_NAME_RESULT","ntdsapi/DS_NAME_RESULTA","ntdsapi/DS_NAME_RESULTW","ntdsapi/PDS_NAME_RESULT"]
old-location: ad\ds_name_result.htm
tech.root: ad
ms.assetid: 8c3cedae-f998-482c-95db-33bca94e119b
ms.date: 12/05/2018
ms.keywords: '*PDS_NAME_RESULTA, DS_NAME_RESULT, DS_NAME_RESULT structure [Active Directory], DS_NAME_RESULTA, DS_NAME_RESULTW, PDS_NAME_RESULT, PDS_NAME_RESULT structure pointer [Active Directory], _glines_ds_name_result, ad.ds__name__result, ad.ds_name_result, ntdsapi/DS_NAME_RESULT, ntdsapi/DS_NAME_RESULTA, ntdsapi/DS_NAME_RESULTW, ntdsapi/PDS_NAME_RESULT'
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DS_NAME_RESULTW (Unicode) and DS_NAME_RESULTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DS_NAME_RESULTA, *PDS_NAME_RESULTA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDS_NAME_RESULTA
 - ntdsapi/PDS_NAME_RESULTA
 - DS_NAME_RESULTA
 - ntdsapi/DS_NAME_RESULTA
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
 - DS_NAME_RESULT
 - DS_NAME_RESULTA
 - DS_NAME_RESULTW
---

# DS_NAME_RESULTA structure


## -description

The <b>DS_NAME_RESULT</b> structure is used with the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a> function to contain the  names converted by the function.

## -struct-fields

### -field cItems

Contains the number of elements in the <b>rItems</b> array.

### -field size_is

### -field size_is.cItems

### -field rItems

Contains an array of <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_result_itema">DS_NAME_RESULT_ITEM</a> structure pointers. Each element of this array represents a single converted name.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_result_itema">DS_NAME_RESULT_ITEM</a>



<a href="/windows/desktop/AD/domain-controller-and-replication-management-structures">Domain Controller and Replication Management Structures</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DS_NAME_RESULT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

