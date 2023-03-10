---
UID: NS:mmc._MMC_COLUMN_DATA
title: MMC_COLUMN_DATA (mmc.h)
description: The MMC_COLUMN_DATA structure is introduced in MMC 1.2.
helpviewer_keywords: ["MMC_COLUMN_DATA","MMC_COLUMN_DATA structure [MMC]","_slate_mmc_column_data","mmc.mmc_column_data","mmc/MMC_COLUMN_DATA"]
old-location: mmc\mmc_column_data.htm
tech.root: mmc
ms.assetid: 93825514-1732-4a07-a323-d4f0cdfe955e
ms.date: 12/05/2018
ms.keywords: MMC_COLUMN_DATA, MMC_COLUMN_DATA structure [MMC], _slate_mmc_column_data, mmc.mmc_column_data, mmc/MMC_COLUMN_DATA
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
req.typenames: MMC_COLUMN_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_COLUMN_DATA
 - mmc/_MMC_COLUMN_DATA
 - MMC_COLUMN_DATA
 - mmc/MMC_COLUMN_DATA
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
 - MMC_COLUMN_DATA
---

# MMC_COLUMN_DATA structure


## -description

The 
MMC_COLUMN_DATA structure is introduced in MMC 1.2.

The 
MMC_COLUMN_DATA structure contains the column data of a single column in a column set. The column data is persisted in memory by MMC. The 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_column_set_data">MMC_COLUMN_SET_DATA</a> structure holds a pointer to an array of 
MMC_COLUMN_DATA structures.

## -struct-fields

### -field nColIndex

A zero-based index value of the column.

### -field dwFlags

A flag that is defined, HDI_HIDDEN (= 0x0001), which indicates that the column is hidden. The default value for the field is 0, indicating that the column is visible.

### -field nWidth

Width of the column.

### -field ulReserved

Not currently used.

## -remarks

By setting the dwFlags member of the 
MMC_COLUMN_DATA structure, a snap-in can hide or show columns in a column set in calls to 
<a href="/windows/desktop/api/mmc/nf-mmc-icolumndata-setcolumnconfigdata">IColumnData::SetColumnConfigData</a>. However, column "0" of a column set cannot be hidden. This is to ensure that result pane icons are properly inserted in the first column and that the MMC_VERB_RENAME console verb functions properly.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/ccf-column-set-id">CCF_COLUMN_SET_ID</a>



<a href="/windows/desktop/api/mmc/ns-mmc-mmc_column_set_data">MMC_COLUMN_SET_DATA</a>



<a href="/previous-versions/windows/desktop/mmc/using-column-persistence">Using Column Persistence</a>