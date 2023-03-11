---
UID: NE:mmc._MMC_TASK_DISPLAY_TYPE
title: MMC_TASK_DISPLAY_TYPE (mmc.h)
description: The MMC_TASK_DISPLAY_TYPE enumeration is introduced in MMC 1.1.
helpviewer_keywords: ["MMC_TASK_DISPLAY_TYPE","MMC_TASK_DISPLAY_TYPE enumeration [MMC]","MMC_TASK_DISPLAY_TYPE_BITMAP","MMC_TASK_DISPLAY_TYPE_CHOCOLATE_GIF","MMC_TASK_DISPLAY_TYPE_SYMBOL","MMC_TASK_DISPLAY_TYPE_VANILLA_GIF","MMC_TASK_DISPLAY_UNINITIALIZED","_slate_mmc_task_display_type","mmc.mmc_task_display_type","mmc/MMC_TASK_DISPLAY_TYPE","mmc/MMC_TASK_DISPLAY_TYPE_BITMAP","mmc/MMC_TASK_DISPLAY_TYPE_CHOCOLATE_GIF","mmc/MMC_TASK_DISPLAY_TYPE_SYMBOL","mmc/MMC_TASK_DISPLAY_TYPE_VANILLA_GIF","mmc/MMC_TASK_DISPLAY_UNINITIALIZED"]
old-location: mmc\mmc_task_display_type.htm
tech.root: mmc
ms.assetid: 55d90530-5cd0-42ae-8a5d-417f7f49edac
ms.date: 12/05/2018
ms.keywords: MMC_TASK_DISPLAY_TYPE, MMC_TASK_DISPLAY_TYPE enumeration [MMC], MMC_TASK_DISPLAY_TYPE_BITMAP, MMC_TASK_DISPLAY_TYPE_CHOCOLATE_GIF, MMC_TASK_DISPLAY_TYPE_SYMBOL, MMC_TASK_DISPLAY_TYPE_VANILLA_GIF, MMC_TASK_DISPLAY_UNINITIALIZED, _slate_mmc_task_display_type, mmc.mmc_task_display_type, mmc/MMC_TASK_DISPLAY_TYPE, mmc/MMC_TASK_DISPLAY_TYPE_BITMAP, mmc/MMC_TASK_DISPLAY_TYPE_CHOCOLATE_GIF, mmc/MMC_TASK_DISPLAY_TYPE_SYMBOL, mmc/MMC_TASK_DISPLAY_TYPE_VANILLA_GIF, mmc/MMC_TASK_DISPLAY_UNINITIALIZED
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
req.typenames: MMC_TASK_DISPLAY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_TASK_DISPLAY_TYPE
 - mmc/_MMC_TASK_DISPLAY_TYPE
 - MMC_TASK_DISPLAY_TYPE
 - mmc/MMC_TASK_DISPLAY_TYPE
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
 - MMC_TASK_DISPLAY_TYPE
---

# MMC_TASK_DISPLAY_TYPE enumeration


## -description

The 
<b>MMC_TASK_DISPLAY_TYPE</b> enumeration is introduced in MMC 1.1.

The 
<b>MMC_TASK_DISPLAY_TYPE</b> enumeration defines the types of image that can be displayed for a task or the background on a taskpad. These values are used in the <b>eDisplayType</b> member of the 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_object">MMC_TASK_DISPLAY_OBJECT</a> structure.

For that which displays the task image, the 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_object">MMC_TASK_DISPLAY_OBJECT</a> structure is the <b>sDisplayObject</b> member of the 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task">MMC_TASK</a> structure, which is filled in by the 
<a href="/windows/desktop/api/mmc/nf-mmc-ienumtask-next">IEnumTASK::Next</a> method.

For that which displays the background image, the 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_object">MMC_TASK_DISPLAY_OBJECT</a> structure is filled in by the 
<a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-getbackground">IExtendTaskPad::GetBackground</a> method.

## -enum-fields

### -field MMC_TASK_DISPLAY_UNINITIALIZED:0

No images specified.

### -field MMC_TASK_DISPLAY_TYPE_SYMBOL

The image displayed for the task or background is the symbol specified by an 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_symbol">MMC_TASK_DISPLAY_SYMBOL</a> structure.

### -field MMC_TASK_DISPLAY_TYPE_VANILLA_GIF

The image displayed for the task or background is a transparent GIF image.

The GIF image is specified by an 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_bitmap">MMC_TASK_DISPLAY_BITMAP</a> structure.

<div class="alert"><b>Note</b>  There is no difference between <b>MMC_TASK_DISPLAY_TYPE_VANILLA_GIF</b> and <b>MMC_TASK_DISPLAY_TYPE_CHOCOLATE_GIF</b>.</div>
<div> </div>

### -field MMC_TASK_DISPLAY_TYPE_CHOCOLATE_GIF

The image displayed for the task or background is a transparent GIF image.

The GIF image is specified by an 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_bitmap">MMC_TASK_DISPLAY_BITMAP</a> structure.

<div class="alert"><b>Note</b>  There is no difference between <b>MMC_TASK_DISPLAY_TYPE_VANILLA_GIF</b> and <b>MMC_TASK_DISPLAY_TYPE_CHOCOLATE_GIF</b>.</div>
<div> </div>

### -field MMC_TASK_DISPLAY_TYPE_BITMAP

The image displayed for the task or background is a nontransparent bitmap image.

The bitmap image is specified by an 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_bitmap">MMC_TASK_DISPLAY_BITMAP</a> structure.
