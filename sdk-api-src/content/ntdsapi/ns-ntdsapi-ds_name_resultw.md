---
UID: NS:ntdsapi.DS_NAME_RESULTW
title: DS_NAME_RESULTW
author: windows-driver-content
description: The DS_NAME_RESULT structure is used with the DsCrackNames function to contain the names converted by the function.
old-location: ad\ds_name_result.htm
old-project: AD
ms.assetid: 8c3cedae-f998-482c-95db-33bca94e119b
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: "*PDS_NAME_RESULTW, DS_NAME_RESULT, DS_NAME_RESULT structure [Active Directory], DS_NAME_RESULTA, DS_NAME_RESULTW, PDS_NAME_RESULT, PDS_NAME_RESULT structure pointer [Active Directory], _glines_ds_name_result, ad.ds__name__result, ad.ds_name_result, ntdsapi/DS_NAME_RESULT, ntdsapi/DS_NAME_RESULTA, ntdsapi/DS_NAME_RESULTW, ntdsapi/PDS_NAME_RESULT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: DS_NAME_RESULTW, *PDS_NAME_RESULTW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntdsapi.h
api_name:
-	DS_NAME_RESULT
-	DS_NAME_RESULTA
-	DS_NAME_RESULTW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DS_NAME_RESULTW structure


## -description


The <b>DS_NAME_RESULT</b> structure is used with the <a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a> function to contain the  names converted by the function.


## -struct-fields




### -field cItems

Contains the number of elements in the <b>rItems</b> array.


### -field rItems.size_is

 


### -field rItems.size_is.cItems

 


### -field rItems

Contains an array of <a href="https://msdn.microsoft.com/50a4488f-e2d4-4671-b0e7-fb8cb4096c5c">DS_NAME_RESULT_ITEM</a> structure pointers. Each element of this array represents a single converted name.


## -see-also




<a href="https://msdn.microsoft.com/50a4488f-e2d4-4671-b0e7-fb8cb4096c5c">DS_NAME_RESULT_ITEM</a>



<a href="https://msdn.microsoft.com/42b20d3b-1799-4f5f-b74e-fe9284dd8ac3">Domain Controller and Replication Management Structures</a>



<a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a>
 

 

