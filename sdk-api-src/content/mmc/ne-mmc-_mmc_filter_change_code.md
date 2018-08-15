---
UID: NE:mmc._MMC_FILTER_CHANGE_CODE
title: "_MMC_FILTER_CHANGE_CODE"
author: windows-sdk-content
description: The MMC_FILTER_CHANGE_CODE enumeration is introduced in MMC 1.2.
old-location: mmc\mmc_filter_change_code.htm
old-project: MMC
ms.assetid: 04f3daf3-2ac0-4999-9a08-1b46f1ef47c8
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: MFCC_DISABLE, MFCC_ENABLE, MFCC_VALUE_CHANGE, MMC_FILTER_CHANGE_CODE, MMC_FILTER_CHANGE_CODE enumeration [MMC], _MMC_FILTER_CHANGE_CODE, _slate_mmc_filter_change_code, mmc.mmc_filter_change_code, mmc/MFCC_DISABLE, mmc/MFCC_ENABLE, mmc/MFCC_VALUE_CHANGE, mmc/MMC_FILTER_CHANGE_CODE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mmc.h
req.include-header: 
req.redist: 
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
req.typenames: MMC_FILTER_CHANGE_CODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_FILTER_CHANGE_CODE
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MMC_FILTER_CHANGE_CODE enumeration


## -description


The 
<b>MMC_FILTER_CHANGE_CODE</b> enumeration is introduced in MMC 1.2.

The 
<b>MMC_FILTER_CHANGE_CODE</b> enumeration specifies the filter change codes that can be sent as the <i>arg</i> parameter of an 
<a href="https://msdn.microsoft.com/b779f04c-1129-4e05-83c5-fd15ff72f1c2">MMCN_FILTER_CHANGE</a> notification in calls to 
<a href="https://msdn.microsoft.com/38c3b31f-356c-46cf-904a-98241c0f199f">IComponent::Notify</a>.


## -enum-fields




### -field MFCC_DISABLE

The filter view has been turned off.


### -field MFCC_ENABLE

The filter view has been turned on.


### -field MFCC_VALUE_CHANGE

The filter value of a column in a result view filter list has changed. The <i>param</i> parameter of the 
<a href="https://msdn.microsoft.com/38c3b31f-356c-46cf-904a-98241c0f199f">IComponent::Notify</a> method contains the column ID.


## -see-also




<a href="https://msdn.microsoft.com/4be29e44-7e64-4c2c-820b-26c6cfea0661">Adding Filtered Views</a>



<a href="https://msdn.microsoft.com/b779f04c-1129-4e05-83c5-fd15ff72f1c2">MMCN_FILTER_CHANGE</a>
 

 

