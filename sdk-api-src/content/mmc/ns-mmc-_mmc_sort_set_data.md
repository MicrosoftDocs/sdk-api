---
UID: NS:mmc._MMC_SORT_SET_DATA
title: "_MMC_SORT_SET_DATA"
author: windows-sdk-content
description: Used with setting and retrieving list view column sets whose sort data is stored persistently.
old-location: mmc\mmc_sort_set_data.htm
old-project: MMC
ms.assetid: bb16061d-a6bb-4816-b52d-c63097638f58
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: 0, 1, MMC_SORT_SET_DATA, MMC_SORT_SET_DATA structure [MMC], _MMC_SORT_SET_DATA, _slate_mmc_sort_set_data, mmc.mmc_sort_set_data, mmc/MMC_SORT_SET_DATA
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
req.typenames: MMC_SORT_SET_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_SORT_SET_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MMC_SORT_SET_DATA structure


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
<a href="https://msdn.microsoft.com/26500d98-4355-4e0c-a636-2c6898955ef0">MMC_SORT_DATA</a> structures that hold the actual sort data. Should be set to <b>NULL</b> if nNumItems is set to 0.


## -remarks



MMC 1.2 only supports single-column sorting, so the nNumItems member of the 
MMC_SORT_SET_DATA structure cannot be greater than 1. Otherwise, 
<a href="https://msdn.microsoft.com/ece69cce-6861-4795-b1cb-da22d2bdc67a">IColumnData::SetColumnSortData</a> will return S_FALSE.

Sorting is disabled on hidden columns. Columns can be hidden or displayed using the 
<a href="https://msdn.microsoft.com/2f6727bd-b7ba-4e91-9dce-53605b0b6fe1">IColumnData::SetColumnConfigData</a> method.

The user can hide columns using the Choose Columns dialog.




## -see-also




<a href="https://msdn.microsoft.com/e4fc2b5f-2736-4a5b-adaa-f1c87d55f0b8">CCF_COLUMN_SET_ID</a>



<a href="https://msdn.microsoft.com/26500d98-4355-4e0c-a636-2c6898955ef0">MMC_SORT_DATA</a>



<a href="https://msdn.microsoft.com/409b8212-a2fc-4d64-a407-ade2fde9ac4d">Using Column Persistence</a>
 

 

