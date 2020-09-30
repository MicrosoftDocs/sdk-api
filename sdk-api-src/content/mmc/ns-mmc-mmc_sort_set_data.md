---
UID: NS:mmc._MMC_SORT_SET_DATA
title: MMC_SORT_SET_DATA (mmc.h)
description: Used with setting and retrieving list view column sets whose sort data is stored persistently.
helpviewer_keywords: ["0","1","MMC_SORT_SET_DATA","MMC_SORT_SET_DATA structure [MMC]","_slate_mmc_sort_set_data","mmc.mmc_sort_set_data","mmc/MMC_SORT_SET_DATA"]
old-location: mmc\mmc_sort_set_data.htm
tech.root: mmc
ms.assetid: bb16061d-a6bb-4816-b52d-c63097638f58
ms.date: 12/05/2018
ms.keywords: 0, 1, MMC_SORT_SET_DATA, MMC_SORT_SET_DATA structure [MMC], _slate_mmc_sort_set_data, mmc.mmc_sort_set_data, mmc/MMC_SORT_SET_DATA
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
req.typenames: MMC_SORT_SET_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_SORT_SET_DATA
 - mmc/_MMC_SORT_SET_DATA
 - MMC_SORT_SET_DATA
 - mmc/MMC_SORT_SET_DATA
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
 - MMC_SORT_SET_DATA
---

# MMC_SORT_SET_DATA structure


## -description

The 
MMC_SORT_SET_DATA structure is introduced in MMC 1.2.

The 
MMC_SORT_SET_DATA structure is used with setting and retrieving list view column sets whose sort data is stored persistently. The 
MMC_SORT_SET_DATA structure contains information about the number of columns in a particular column set for which persistent sort data is being set or retrieved, as well as a pointer to an array of 
MMC_SORT_DATA structures that actually hold the sort data.

## -struct-fields

### -field cbSize

Size of the 
MMC_SORT_SET_DATA structure.

### -field nNumItems

The number of columns in the column set for which persistent sort data is being set or retrieved. This value can be one of the following:



#### 0

No columns in the column set are sorted. The snap-in can set nNumItems to this value to persist the fact that the list view is not sorted. In this case, the pSortData member should be set to <b>NULL</b>.



#### 1

One column in the column set is sorted. Be aware that only single-column sorting is allowed in MMC 1.2.

### -field pSortData

A pointer to an array of 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_sort_data">MMC_SORT_DATA</a> structures that hold the actual sort data. Should be set to <b>NULL</b> if nNumItems is set to 0.

## -remarks

MMC 1.2 only supports single-column sorting, so the nNumItems member of the 
MMC_SORT_SET_DATA structure cannot be greater than 1. Otherwise, 
<a href="/windows/desktop/api/mmc/nf-mmc-icolumndata-setcolumnsortdata">IColumnData::SetColumnSortData</a> will return S_FALSE.

Sorting is disabled on hidden columns. Columns can be hidden or displayed using the 
<a href="/windows/desktop/api/mmc/nf-mmc-icolumndata-setcolumnconfigdata">IColumnData::SetColumnConfigData</a> method.

The user can hide columns using the Choose Columns dialog.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/ccf-column-set-id">CCF_COLUMN_SET_ID</a>



<a href="/windows/desktop/api/mmc/ns-mmc-mmc_sort_data">MMC_SORT_DATA</a>



<a href="/previous-versions/windows/desktop/mmc/using-column-persistence">Using Column Persistence</a>