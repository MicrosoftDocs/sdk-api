---
UID: NS:mmc._MMC_TASK_DISPLAY_OBJECT
title: MMC_TASK_DISPLAY_OBJECT (mmc.h)
description: Specifies the type of image and all the data required to use that image to display a task or the background on a taskpad.
helpviewer_keywords: ["MMC_TASK_DISPLAY_OBJECT","MMC_TASK_DISPLAY_OBJECT structure [MMC]","_slate_mmc_task_display_object","mmc.mmc_task_display_object","mmc/MMC_TASK_DISPLAY_OBJECT"]
old-location: mmc\mmc_task_display_object.htm
tech.root: mmc
ms.assetid: ff43f0ea-2f33-4ed9-b5a5-484db2ffe3ad
ms.date: 12/05/2018
ms.keywords: MMC_TASK_DISPLAY_OBJECT, MMC_TASK_DISPLAY_OBJECT structure [MMC], _slate_mmc_task_display_object, mmc.mmc_task_display_object, mmc/MMC_TASK_DISPLAY_OBJECT
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
req.typenames: MMC_TASK_DISPLAY_OBJECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_TASK_DISPLAY_OBJECT
 - mmc/_MMC_TASK_DISPLAY_OBJECT
 - MMC_TASK_DISPLAY_OBJECT
 - mmc/MMC_TASK_DISPLAY_OBJECT
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
 - MMC_TASK_DISPLAY_OBJECT
---

# MMC_TASK_DISPLAY_OBJECT structure


## -description

The 
<b>MMC_TASK_DISPLAY_OBJECT</b> structure is introduced in MMC 1.1.

The 
<b>MMC_TASK_DISPLAY_OBJECT</b> structure specifies the type of image and all the data required to use that image to display a task or the background on a taskpad.

For that which displays the task image, the 
<b>MMC_TASK_DISPLAY_OBJECT</b> structure is the <b>sDisplayObject</b> member of the 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task">MMC_TASK</a> structure, which is filled in by the 
<a href="/windows/desktop/api/mmc/nf-mmc-ienumtask-next">IEnumTASK::Next</a> method.

For that which displays the background image, the 
<b>MMC_TASK_DISPLAY_OBJECT</b> structure is filled in by the 
<a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-getbackground">IExtendTaskPad::GetBackground</a> method.

## -struct-fields

### -field eDisplayType

Value of type 
<a href="/windows/desktop/api/mmc/ne-mmc-mmc_task_display_type">MMC_TASK_DISPLAY_TYPE</a> that specifies the type of image displayed as the background. The image can be one of three types: symbol, GIF, or bitmap.

### -field uBitmap

<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_bitmap">MMC_TASK_DISPLAY_BITMAP</a> structure that contains the resource paths to the image files of the image type specified by <b>eDisplayType</b>. 
<b>MMC_TASK_DISPLAY_BITMAP</b> contains the paths to the two images used when the user moves the mouse over a task and when the task is deselected.

The <b>uBitmap</b> member is used only if <b>eDisplayType</b> is one of the following values:

<ul>
<li><b>MMC_TASK_DISPLAY_TYPE_BITMAP</b></li>
<li><b>MMC_TASK_DISPLAY_TYPE_VANILLA_GIF</b></li>
<li><b>MMC_TASK_DISPLAY_TYPE_CHOCOLATE_GIF</b></li>
</ul>
The <b>MMC_TASK_DISPLAY_TYPE_BITMAP</b> value indicates that a non-transparent image is being used for the task or background. The <b>MMC_TASK_DISPLAY_TYPE_VANILLA_GIF</b> and <b>MMC_TASK_DISPLAY_TYPE_CHOCOLATE_GIF</b> values indicate that a transparent image is being used for the task or background.

<div class="alert"><b>Note</b>  There is no difference between <b>MMC_TASK_DISPLAY_TYPE_VANILLA_GIF</b> and <b>MMC_TASK_DISPLAY_TYPE_CHOCOLATE_GIF</b>.</div>
<div> </div>

### -field uSymbol

<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_symbol">MMC_TASK_DISPLAY_SYMBOL</a> structure that contains the font name, EOT (embedded OpenType) resource path, and characters to display as the image.

The <b>uSymbol</b> is used only if <b>eDisplayType</b> is <b>MMC_TASK_DISPLAY_TYPE_SYMBOL</b>.

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-ienumtask-next">IEnumTASK::Next</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-getbackground">IExtendTaskPad::GetBackground</a>



<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task">MMC_TASK</a>



<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_bitmap">MMC_TASK_DISPLAY_BITMAP</a>



<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_symbol">MMC_TASK_DISPLAY_SYMBOL</a>



<a href="/windows/desktop/api/mmc/ne-mmc-mmc_task_display_type">MMC_TASK_DISPLAY_TYPE</a>