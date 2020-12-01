---
UID: NS:mmc._MMC_TASK_DISPLAY_BITMAP
title: MMC_TASK_DISPLAY_BITMAP (mmc.h)
description: The MMC_TASK_DISPLAY_BITMAP structure is introduced in MMC 1.1.
helpviewer_keywords: ["MMC_TASK_DISPLAY_BITMAP","MMC_TASK_DISPLAY_BITMAP structure [MMC]","_slate_mmc_task_display_bitmap","mmc.mmc_task_display_bitmap","mmc/MMC_TASK_DISPLAY_BITMAP"]
old-location: mmc\mmc_task_display_bitmap.htm
tech.root: mmc
ms.assetid: 9895eef1-7870-4092-8bf9-c13f38b74173
ms.date: 12/05/2018
ms.keywords: MMC_TASK_DISPLAY_BITMAP, MMC_TASK_DISPLAY_BITMAP structure [MMC], _slate_mmc_task_display_bitmap, mmc.mmc_task_display_bitmap, mmc/MMC_TASK_DISPLAY_BITMAP
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
req.typenames: MMC_TASK_DISPLAY_BITMAP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_TASK_DISPLAY_BITMAP
 - mmc/_MMC_TASK_DISPLAY_BITMAP
 - MMC_TASK_DISPLAY_BITMAP
 - mmc/MMC_TASK_DISPLAY_BITMAP
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
 - MMC_TASK_DISPLAY_BITMAP
---

# MMC_TASK_DISPLAY_BITMAP structure


## -description

The 
<b>MMC_TASK_DISPLAY_BITMAP</b> structure is introduced in MMC 1.1.

The 
<b>MMC_TASK_DISPLAY_BITMAP</b> structure is used for the <b>uBitmap</b> member of the 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_object">MMC_TASK_DISPLAY_OBJECT</a> structure to specify all the data required to display a GIF or bitmap image for a task or background on a taskpad.

## -struct-fields

### -field szMouseOverBitmap

A pointer to a null-terminated string that contains the resource path to the image file for the image displayed for the task when the user moves the mouse over the task's image or text area.

The string should have the following form:

"res://<i>filepath</i>/<i>imgpath</i>"

where <i>filepath</i> is the full path to the snap-in's DLL that stores the image file as a resource, and <i>imgpath</i> is the resource path of the image file with the snap-in DLL.

For example, the following string specifies that the snap-in DLL (snapin.dll) has a path of "c:\windows\system32\snapin.dll" and that the resource path is img/mon.gif: "res://c:\\windows\\system32\\snapin.dll/img/mon.bmp".

If <i>szMouseOverBitmap</i> points to a <b>NULL</b> string, <i>szMouseOffBitmap</i> must be a valid string that contains the location of a valid image. If one of these strings is <b>NULL</b>, the other string is used for both. If both mouse image locations are <b>NULL</b>, the task is not displayed.

### -field szMouseOffBitmap

A pointer to a null-terminated string that contains the resource path to the image file for the image displayed for the task when the mouse is not in the task's image or text area.

See <b>szMouseOverBitmap</b> for the format of the string.

If <b>szMouseOffBitmap</b> points to a <b>NULL</b> string, <b>szMouseOverBitmap</b> must be a valid string that contains the location of a valid image. If one of these strings is <b>NULL</b>, the other string is used for both. If both mouse image locations are <b>NULL</b>, the task is not displayed.

## -remarks

Allocate the <b>szMouseOverBitmap</b> and <b>szMouseOffBitmap</b> strings used in the structure with the COM API function <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> (or the equivalent) and MMC will release them.

If both <b>szMouseOverBitmap</b> and <b>szMouseOffBitmap</b> point to a <b>NULL</b> string, the task does not appear on the taskpad. If one of these strings is <b>NULL</b>, the other string is used for both.

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-ienumtask-next">IEnumTASK::Next</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-getbackground">IExtendTaskPad::GetBackground</a>



<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_object">MMC_TASK_DISPLAY_OBJECT</a>



<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_symbol">MMC_TASK_DISPLAY_SYMBOL</a>



<a href="/windows/desktop/api/mmc/ne-mmc-mmc_task_display_type">MMC_TASK_DISPLAY_TYPE</a>