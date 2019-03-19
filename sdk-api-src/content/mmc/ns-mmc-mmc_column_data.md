---
UID: NS:mmc._MMC_COLUMN_DATA
title: MMC_COLUMN_DATA (mmc.h)
author: windows-sdk-content
description: The MMC_COLUMN_DATA structure is introduced in MMC 1.2.
old-location: mmc\mmc_column_data.htm
tech.root: mmc
ms.assetid: 93825514-1732-4a07-a323-d4f0cdfe955e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MMC_COLUMN_DATA, MMC_COLUMN_DATA structure [MMC], _slate_mmc_column_data, mmc.mmc_column_data, mmc/MMC_COLUMN_DATA
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_COLUMN_DATA
product: Windows
targetos: Windows
req.typenames: MMC_COLUMN_DATA
req.redist: 
---

# MMC_COLUMN_DATA structure


## -description


The 
MMC_COLUMN_DATA structure is introduced in MMC 1.2.

The 
MMC_COLUMN_DATA structure contains the column data of a single column in a column set. The column data is persisted in memory by MMC. The 
<a href="https://msdn.microsoft.com/15088a2f-3dfc-4af4-bcae-e7e9e456df8b">MMC_COLUMN_SET_DATA</a> structure holds a pointer to an array of 
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
<a href="https://msdn.microsoft.com/2f6727bd-b7ba-4e91-9dce-53605b0b6fe1">IColumnData::SetColumnConfigData</a>. However, column "0" of a column set cannot be hidden. This is to ensure that result pane icons are properly inserted in the first column and that the MMC_VERB_RENAME console verb functions properly.




## -see-also




<a href="https://msdn.microsoft.com/e4fc2b5f-2736-4a5b-adaa-f1c87d55f0b8">CCF_COLUMN_SET_ID</a>



<a href="https://msdn.microsoft.com/15088a2f-3dfc-4af4-bcae-e7e9e456df8b">MMC_COLUMN_SET_DATA</a>



<a href="https://msdn.microsoft.com/409b8212-a2fc-4d64-a407-ade2fde9ac4d">Using Column Persistence</a>
 

 

