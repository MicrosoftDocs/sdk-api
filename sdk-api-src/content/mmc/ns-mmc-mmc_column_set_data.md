---
UID: NS:mmc._MMC_COLUMN_SET_DATA
title: MMC_COLUMN_SET_DATA (mmc.h)
description: The MMC_COLUMN_SET_DATA structure is introduced in MMC 1.2.
helpviewer_keywords: ["MMC_COLUMN_SET_DATA","MMC_COLUMN_SET_DATA structure [MMC]","_slate_mmc_column_set_data","mmc.mmc_column_set_data","mmc/MMC_COLUMN_SET_DATA"]
old-location: mmc\mmc_column_set_data.htm
tech.root: mmc
ms.assetid: 15088a2f-3dfc-4af4-bcae-e7e9e456df8b
ms.date: 12/05/2018
ms.keywords: MMC_COLUMN_SET_DATA, MMC_COLUMN_SET_DATA structure [MMC], _slate_mmc_column_set_data, mmc.mmc_column_set_data, mmc/MMC_COLUMN_SET_DATA
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
req.typenames: MMC_COLUMN_SET_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_COLUMN_SET_DATA
 - mmc/_MMC_COLUMN_SET_DATA
 - MMC_COLUMN_SET_DATA
 - mmc/MMC_COLUMN_SET_DATA
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
 - MMC_COLUMN_SET_DATA
---

# MMC_COLUMN_SET_DATA structure


## -description

The 
MMC_COLUMN_SET_DATA structure is introduced in MMC 1.2.

The 
MMC_COLUMN_SET_DATA structure is used with setting and retrieving list view column sets whose data is persisted in memory by MMC. The 
MMC_COLUMN_SET_DATA structure contains information about the number of columns in a particular column set as well as a pointer to persisted column data of the column set.

## -struct-fields

### -field cbSize

The size of the 
MMC_COLUMN_SET_DATA structure.

### -field nNumCols

The number of columns in the column set.

### -field pColData

A pointer to an array of 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_column_data">MMC_COLUMN_DATA</a> structures that contains the persisted column set data.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/ccf-column-set-id">CCF_COLUMN_SET_ID</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icolumndata">IColumnData</a>



<a href="/windows/desktop/api/mmc/nf-mmc-icolumndata-getcolumnconfigdata">IColumnData::GetColumnConfigData</a>



<a href="/windows/desktop/api/mmc/nf-mmc-icolumndata-setcolumnconfigdata">IColumnData::SetColumnConfigData</a>



<a href="/previous-versions/windows/desktop/mmc/using-column-persistence">Using Column Persistence</a>