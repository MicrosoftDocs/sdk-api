---
UID: NE:mmc._MMC_TASK_DISPLAY_TYPE
title: "_MMC_TASK_DISPLAY_TYPE"
author: windows-sdk-content
description: The MMC_TASK_DISPLAY_TYPE enumeration is introduced in MMC 1.1.
old-location: mmc\mmc_task_display_type.htm
old-project: MMC
ms.assetid: 55d90530-5cd0-42ae-8a5d-417f7f49edac
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: MMC_TASK_DISPLAY_TYPE, MMC_TASK_DISPLAY_TYPE enumeration [MMC], MMC_TASK_DISPLAY_TYPE_BITMAP, MMC_TASK_DISPLAY_TYPE_CHOCOLATE_GIF, MMC_TASK_DISPLAY_TYPE_SYMBOL, MMC_TASK_DISPLAY_TYPE_VANILLA_GIF, MMC_TASK_DISPLAY_UNINITIALIZED, _MMC_TASK_DISPLAY_TYPE, _slate_mmc_task_display_type, mmc.mmc_task_display_type, mmc/MMC_TASK_DISPLAY_TYPE, mmc/MMC_TASK_DISPLAY_TYPE_BITMAP, mmc/MMC_TASK_DISPLAY_TYPE_CHOCOLATE_GIF, mmc/MMC_TASK_DISPLAY_TYPE_SYMBOL, mmc/MMC_TASK_DISPLAY_TYPE_VANILLA_GIF, mmc/MMC_TASK_DISPLAY_UNINITIALIZED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: MMC_TASK_DISPLAY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_TASK_DISPLAY_TYPE
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MMC_TASK_DISPLAY_TYPE enumeration


## -description


The 
<b>MMC_TASK_DISPLAY_TYPE</b> enumeration is introduced in MMC 1.1.

The 
<b>MMC_TASK_DISPLAY_TYPE</b> enumeration defines the types of image that can be displayed for a task or the background on a taskpad. These values are used in the <b>eDisplayType</b> member of the 
<a href="https://msdn.microsoft.com/ff43f0ea-2f33-4ed9-b5a5-484db2ffe3ad">MMC_TASK_DISPLAY_OBJECT</a> structure.

For that which displays the task image, the 
<a href="https://msdn.microsoft.com/ff43f0ea-2f33-4ed9-b5a5-484db2ffe3ad">MMC_TASK_DISPLAY_OBJECT</a> structure is the <b>sDisplayObject</b> member of the 
<a href="https://msdn.microsoft.com/bb101c09-947f-4316-890a-86e09358d88c">MMC_TASK</a> structure, which is filled in by the 
<a href="https://msdn.microsoft.com/cb568307-7172-4941-a888-ff059f5256b6">IEnumTASK::Next</a> method.

For that which displays the background image, the 
<a href="https://msdn.microsoft.com/ff43f0ea-2f33-4ed9-b5a5-484db2ffe3ad">MMC_TASK_DISPLAY_OBJECT</a> structure is filled in by the 
<a href="https://msdn.microsoft.com/e34fc088-61d7-46a8-b493-8255a733d521">IExtendTaskPad::GetBackground</a> method.


## -enum-fields




### -field MMC_TASK_DISPLAY_UNINITIALIZED

No images specified.


### -field MMC_TASK_DISPLAY_TYPE_SYMBOL

The image displayed for the task or background is the symbol specified by an 
<a href="https://msdn.microsoft.com/a46f1b86-883e-4eca-a3f8-d18c6a4d64e5">MMC_TASK_DISPLAY_SYMBOL</a> structure.


### -field MMC_TASK_DISPLAY_TYPE_VANILLA_GIF

The image displayed for the task or background is a transparent GIF image.

The GIF image is specified by an 
<a href="https://msdn.microsoft.com/9895eef1-7870-4092-8bf9-c13f38b74173">MMC_TASK_DISPLAY_BITMAP</a> structure.

<div class="alert"><b>Note</b>  There is no difference between <b>MMC_TASK_DISPLAY_TYPE_VANILLA_GIF</b> and <b>MMC_TASK_DISPLAY_TYPE_CHOCOLATE_GIF</b>.</div>
<div> </div>

### -field MMC_TASK_DISPLAY_TYPE_CHOCOLATE_GIF

The image displayed for the task or background is a transparent GIF image.

The GIF image is specified by an 
<a href="https://msdn.microsoft.com/9895eef1-7870-4092-8bf9-c13f38b74173">MMC_TASK_DISPLAY_BITMAP</a> structure.

<div class="alert"><b>Note</b>  There is no difference between <b>MMC_TASK_DISPLAY_TYPE_VANILLA_GIF</b> and <b>MMC_TASK_DISPLAY_TYPE_CHOCOLATE_GIF</b>.</div>
<div> </div>

### -field MMC_TASK_DISPLAY_TYPE_BITMAP

The image displayed for the task or background is a nontransparent bitmap image.

The bitmap image is specified by an 
<a href="https://msdn.microsoft.com/9895eef1-7870-4092-8bf9-c13f38b74173">MMC_TASK_DISPLAY_BITMAP</a> structure.

