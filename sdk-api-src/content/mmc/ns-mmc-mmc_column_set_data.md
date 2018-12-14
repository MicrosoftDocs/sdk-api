---
UID: NS:mmc._MMC_COLUMN_SET_DATA
title: MMC_COLUMN_SET_DATA
author: windows-sdk-content
description: The MMC_COLUMN_SET_DATA structure is introduced in MMC 1.2.
old-location: mmc\mmc_column_set_data.htm
tech.root: mmc
ms.assetid: 15088a2f-3dfc-4af4-bcae-e7e9e456df8b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MMC_COLUMN_SET_DATA, MMC_COLUMN_SET_DATA structure [MMC], _slate_mmc_column_set_data, mmc.mmc_column_set_data, mmc/MMC_COLUMN_SET_DATA
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MMC_COLUMN_SET_DATA
product: Windows
targetos: Windows
req.typenames: MMC_COLUMN_SET_DATA
req.redist: 
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
<a href="https://msdn.microsoft.com/93825514-1732-4a07-a323-d4f0cdfe955e">MMC_COLUMN_DATA</a> structures that contains the persisted column set data.


## -see-also




<a href="https://msdn.microsoft.com/e4fc2b5f-2736-4a5b-adaa-f1c87d55f0b8">CCF_COLUMN_SET_ID</a>



<a href="https://msdn.microsoft.com/fb2b8863-c476-4997-915d-329cf66fd945">IColumnData</a>



<a href="https://msdn.microsoft.com/197804a2-63e5-4f0c-9d6d-4abc751a8a82">IColumnData::GetColumnConfigData</a>



<a href="https://msdn.microsoft.com/2f6727bd-b7ba-4e91-9dce-53605b0b6fe1">IColumnData::SetColumnConfigData</a>



<a href="https://msdn.microsoft.com/409b8212-a2fc-4d64-a407-ade2fde9ac4d">Using Column Persistence</a>
 

 

