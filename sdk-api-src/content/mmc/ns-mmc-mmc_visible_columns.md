---
UID: NS:mmc._MMC_VISIBLE_COLUMNS
title: MMC_VISIBLE_COLUMNS (mmc.h)
description: Used by MMC with the MMCN_COLUMNS_CHANGED notification to inform the snap-in which columns in a column set are visible.
helpviewer_keywords: ["MMC_VISIBLE_COLUMNS","MMC_VISIBLE_COLUMNS structure [MMC]","_slate_mmc_visible_columns","mmc.mmc_visible_columns","mmc/MMC_VISIBLE_COLUMNS"]
old-location: mmc\mmc_visible_columns.htm
tech.root: mmc
ms.assetid: b2f54c36-a446-4c16-8595-ab7e3411eb88
ms.date: 12/05/2018
ms.keywords: MMC_VISIBLE_COLUMNS, MMC_VISIBLE_COLUMNS structure [MMC], _slate_mmc_visible_columns, mmc.mmc_visible_columns, mmc/MMC_VISIBLE_COLUMNS
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
req.typenames: MMC_VISIBLE_COLUMNS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_VISIBLE_COLUMNS
 - mmc/_MMC_VISIBLE_COLUMNS
 - MMC_VISIBLE_COLUMNS
 - mmc/MMC_VISIBLE_COLUMNS
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
 - MMC_VISIBLE_COLUMNS
---

# MMC_VISIBLE_COLUMNS structure


## -description

The 
MMC_VISIBLE_COLUMNS structure is introduced in MMC 1.2.

The 
MMC_VISIBLE_COLUMNS structure is used by MMC with the 
<a href="/previous-versions/windows/desktop/mmc/mmcn-columns-changed">MMCN_COLUMNS_CHANGED</a> notification to inform the snap-in which columns in a column set are visible.

## -struct-fields

### -field nVisibleColumns

The number of visible columns in the column set.

### -field rgVisibleCols

A variable-length array in which each member contains the zero-based number of a visible column. The ordering of the columns in the array corresponds to the order of the columns as they appear in the list view. The nVisibleColumns member gives the number of elements in the list.

## -remarks

The value of rgVisibleCols[0] is always 0 (zero), indicating that the first visible column in the list view is always the zero index-valued column, which must always be the first column and must always be visible. Furthermore, MMC does not allow the user to change the position of the first column.

The order of visible columns may be different than the order of insertion by the snap-in because the user may have rearranged the columns by dragging and dropping their headers.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/mmcn-columns-changed">MMCN_COLUMNS_CHANGED</a>



<a href="/previous-versions/windows/desktop/mmc/using-column-persistence">Using Column Persistence</a>