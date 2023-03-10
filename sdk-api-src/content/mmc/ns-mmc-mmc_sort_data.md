---
UID: NS:mmc._MMC_SORT_DATA
title: MMC_SORT_DATA (mmc.h)
description: Contains the column sort data of a single column in a column set.
helpviewer_keywords: ["MMC_SORT_DATA","MMC_SORT_DATA structure [MMC]","RSI_DESCENDING = 0x0001","RSI_NOSORTICON = 0x0002","_slate_mmc_sort_data","mmc.mmc_sort_data","mmc/MMC_SORT_DATA"]
old-location: mmc\mmc_sort_data.htm
tech.root: mmc
ms.assetid: 26500d98-4355-4e0c-a636-2c6898955ef0
ms.date: 12/05/2018
ms.keywords: MMC_SORT_DATA, MMC_SORT_DATA structure [MMC], RSI_DESCENDING = 0x0001, RSI_NOSORTICON = 0x0002, _slate_mmc_sort_data, mmc.mmc_sort_data, mmc/MMC_SORT_DATA
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MMC_SORT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_SORT_DATA
 - mmc/_MMC_SORT_DATA
 - MMC_SORT_DATA
 - mmc/MMC_SORT_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_SORT_DATA
---

# MMC_SORT_DATA structure


## -description

The 
MMC_SORT_DATA structure is introduced in MMC 1.2.

The 
MMC_SORT_DATA structure contains the column sort data of a single column in a column set. This data is persisted in memory by MMC. A pointer to an array of these structures is held in the pSortData member of the 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_sort_set_data">MMC_SORT_SET_DATA</a> structure.

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

<a href="/previous-versions/windows/desktop/mmc/ccf-column-set-id">CCF_COLUMN_SET_ID</a>



<a href="/windows/desktop/api/mmc/ns-mmc-mmc_sort_set_data">MMC_SORT_SET_DATA</a>



<a href="/previous-versions/windows/desktop/mmc/using-column-persistence">Using Column Persistence</a>