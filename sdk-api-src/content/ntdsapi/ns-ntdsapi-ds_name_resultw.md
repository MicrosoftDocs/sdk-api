---
UID: NS:ntdsapi.__unnamed_struct_3
title: DS_NAME_RESULTW (ntdsapi.h)
description: The DS_NAME_RESULT structure is used with the DsCrackNames function to contain the names converted by the function.
old-location: ad\ds_name_result.htm
tech.root: ad
ms.assetid: 8c3cedae-f998-482c-95db-33bca94e119b
ms.date: 12/05/2018
ms.keywords: '*PDS_NAME_RESULTW, DS_NAME_RESULT, DS_NAME_RESULT structure [Active Directory], DS_NAME_RESULTA, DS_NAME_RESULTW, PDS_NAME_RESULT, PDS_NAME_RESULT structure pointer [Active Directory], _glines_ds_name_result, ad.ds__name__result, ad.ds_name_result, ntdsapi/DS_NAME_RESULT, ntdsapi/DS_NAME_RESULTA, ntdsapi/DS_NAME_RESULTW, ntdsapi/PDS_NAME_RESULT'
ms.topic: struct
f1_keywords:
- ntdsapi/DS_NAME_RESULT
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
req.unicode-ansi: DS_NAME_RESULTW (Unicode) and DS_NAME_RESULTA (ANSI)
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
- DS_NAME_RESULT
- DS_NAME_RESULTA
- DS_NAME_RESULTW
targetos: Windows
req.typenames: DS_NAME_RESULTW, *PDS_NAME_RESULTW
req.redist: 
ms.custom: 19H1
---

# DS_NAME_RESULTW structure


## -description


The <b>DS_NAME_RESULT</b> structure is used with the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a> function to contain the  names converted by the function.


## -struct-fields




### -field cItems

Contains the number of elements in the <b>rItems</b> array.


### -field size_is

 


### -field size_is.cItems

 


### -field rItems

Contains an array of <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_result_itema">DS_NAME_RESULT_ITEM</a> structure pointers. Each element of this array represents a single converted name.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_result_itema">DS_NAME_RESULT_ITEM</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/domain-controller-and-replication-management-structures">Domain Controller and Replication Management Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a>
 

 

