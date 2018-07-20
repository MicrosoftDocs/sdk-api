---
UID: NS:mmc._MMC_SORT_DATA
title: "_MMC_SORT_DATA"
author: windows-sdk-content
description: Contains the column sort data of a single column in a column set.
old-location: mmc\mmc_sort_data.htm
old-project: mmc
ms.assetid: 26500d98-4355-4e0c-a636-2c6898955ef0
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: MMC_SORT_DATA, MMC_SORT_DATA structure [MMC], RSI_DESCENDING = 0x0001, RSI_NOSORTICON = 0x0002, _MMC_SORT_DATA, _slate_mmc_sort_data, mmc.mmc_sort_data, mmc/MMC_SORT_DATA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MMC_SORT_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_SORT_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MMC_SORT_DATA structure


## -description


The 
MMC_SORT_DATA structure is introduced in MMC 1.2.

The 
MMC_SORT_DATA structure contains the column sort data of a single column in a column set. This data is persisted in memory by MMC. A pointer to an array of these structures is held in the pSortData member of the 
<a href="https://msdn.microsoft.com/bb16061d-a6bb-4816-b52d-c63097638f58">MMC_SORT_SET_DATA</a> structure.


## -struct-fields




### -field nColIndex

A zero-based index value of the column.


### -field dwSortOptions

Sort options to be used during the sort operation. This value can be a combination of the following:



#### RSI_DESCENDING = 0x0001

The sort should be in descending order. The default is to sort in ascending order.



#### RSI_NOSORTICON = 0x0002

Instructs MMC to remove the sort arrow icon. This option is useful when the snap-in performs a custom sort operation.


### -field ulReserved

Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/e4fc2b5f-2736-4a5b-adaa-f1c87d55f0b8">CCF_COLUMN_SET_ID</a>



<a href="https://msdn.microsoft.com/bb16061d-a6bb-4816-b52d-c63097638f58">MMC_SORT_SET_DATA</a>



<a href="https://msdn.microsoft.com/409b8212-a2fc-4d64-a407-ade2fde9ac4d">Using Column Persistence</a>
 

 

