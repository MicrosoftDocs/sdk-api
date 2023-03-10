---
UID: NE:mmc._MMC_FILTER_CHANGE_CODE
title: MMC_FILTER_CHANGE_CODE (mmc.h)
description: The MMC_FILTER_CHANGE_CODE enumeration is introduced in MMC 1.2.
helpviewer_keywords: ["MFCC_DISABLE","MFCC_ENABLE","MFCC_VALUE_CHANGE","MMC_FILTER_CHANGE_CODE","MMC_FILTER_CHANGE_CODE enumeration [MMC]","_slate_mmc_filter_change_code","mmc.mmc_filter_change_code","mmc/MFCC_DISABLE","mmc/MFCC_ENABLE","mmc/MFCC_VALUE_CHANGE","mmc/MMC_FILTER_CHANGE_CODE"]
old-location: mmc\mmc_filter_change_code.htm
tech.root: mmc
ms.assetid: 04f3daf3-2ac0-4999-9a08-1b46f1ef47c8
ms.date: 12/05/2018
ms.keywords: MFCC_DISABLE, MFCC_ENABLE, MFCC_VALUE_CHANGE, MMC_FILTER_CHANGE_CODE, MMC_FILTER_CHANGE_CODE enumeration [MMC], _slate_mmc_filter_change_code, mmc.mmc_filter_change_code, mmc/MFCC_DISABLE, mmc/MFCC_ENABLE, mmc/MFCC_VALUE_CHANGE, mmc/MMC_FILTER_CHANGE_CODE
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
req.typenames: MMC_FILTER_CHANGE_CODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_FILTER_CHANGE_CODE
 - mmc/_MMC_FILTER_CHANGE_CODE
 - MMC_FILTER_CHANGE_CODE
 - mmc/MMC_FILTER_CHANGE_CODE
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
 - MMC_FILTER_CHANGE_CODE
---

# MMC_FILTER_CHANGE_CODE enumeration


## -description

The 
<b>MMC_FILTER_CHANGE_CODE</b> enumeration is introduced in MMC 1.2.

The 
<b>MMC_FILTER_CHANGE_CODE</b> enumeration specifies the filter change codes that can be sent as the <i>arg</i> parameter of an 
<a href="/previous-versions/windows/desktop/mmc/mmcn-filter-change">MMCN_FILTER_CHANGE</a> notification in calls to 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-notify">IComponent::Notify</a>.

## -enum-fields

### -field MFCC_DISABLE:0

The filter view has been turned off.

### -field MFCC_ENABLE:1

The filter view has been turned on.

### -field MFCC_VALUE_CHANGE:2

The filter value of a column in a result view filter list has changed. The <i>param</i> parameter of the 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-notify">IComponent::Notify</a> method contains the column ID.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/adding-filtered-views">Adding Filtered Views</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-filter-change">MMCN_FILTER_CHANGE</a>
