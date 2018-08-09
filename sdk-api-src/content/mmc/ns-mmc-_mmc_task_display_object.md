---
UID: NS:mmc._MMC_TASK_DISPLAY_OBJECT
title: "_MMC_TASK_DISPLAY_OBJECT"
author: windows-sdk-content
description: Specifies the type of image and all the data required to use that image to display a task or the background on a taskpad.
old-location: mmc\mmc_task_display_object.htm
old-project: MMC
ms.assetid: ff43f0ea-2f33-4ed9-b5a5-484db2ffe3ad
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: MMC_TASK_DISPLAY_OBJECT, MMC_TASK_DISPLAY_OBJECT structure [MMC], _MMC_TASK_DISPLAY_OBJECT, _slate_mmc_task_display_object, mmc.mmc_task_display_object, mmc/MMC_TASK_DISPLAY_OBJECT
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MMC_TASK_DISPLAY_OBJECT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_TASK_DISPLAY_OBJECT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MMC_TASK_DISPLAY_OBJECT structure


## -description


The 
<b>MMC_TASK_DISPLAY_OBJECT</b> structure is introduced in MMC 1.1.

The 
<b>MMC_TASK_DISPLAY_OBJECT</b> structure specifies the type of image and all the data required to use that image to display a task or the background on a taskpad.

For that which displays the task image, the 
<b>MMC_TASK_DISPLAY_OBJECT</b> structure is the <b>sDisplayObject</b> member of the 
<a href="https://msdn.microsoft.com/bb101c09-947f-4316-890a-86e09358d88c">MMC_TASK</a> structure, which is filled in by the 
<a href="https://msdn.microsoft.com/cb568307-7172-4941-a888-ff059f5256b6">IEnumTASK::Next</a> method.

For that which displays the background image, the 
<b>MMC_TASK_DISPLAY_OBJECT</b> structure is filled in by the 
<a href="https://msdn.microsoft.com/e34fc088-61d7-46a8-b493-8255a733d521">IExtendTaskPad::GetBackground</a> method.


## -struct-fields




### -field eDisplayType

Value of type 
<a href="https://msdn.microsoft.com/55d90530-5cd0-42ae-8a5d-417f7f49edac">MMC_TASK_DISPLAY_TYPE</a> that specifies the type of image displayed as the background. The image can be one of three types: symbol, GIF, or bitmap.


### -field uBitmap


<a href="https://msdn.microsoft.com/9895eef1-7870-4092-8bf9-c13f38b74173">MMC_TASK_DISPLAY_BITMAP</a> structure that contains the resource paths to the image files of the image type specified by <b>eDisplayType</b>. 
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


<a href="https://msdn.microsoft.com/a46f1b86-883e-4eca-a3f8-d18c6a4d64e5">MMC_TASK_DISPLAY_SYMBOL</a> structure that contains the font name, EOT (embedded OpenType) resource path, and characters to display as the image.

The <b>uSymbol</b> is used only if <b>eDisplayType</b> is <b>MMC_TASK_DISPLAY_TYPE_SYMBOL</b>.


## -see-also




<a href="https://msdn.microsoft.com/cb568307-7172-4941-a888-ff059f5256b6">IEnumTASK::Next</a>



<a href="https://msdn.microsoft.com/e34fc088-61d7-46a8-b493-8255a733d521">IExtendTaskPad::GetBackground</a>



<a href="https://msdn.microsoft.com/bb101c09-947f-4316-890a-86e09358d88c">MMC_TASK</a>



<a href="https://msdn.microsoft.com/9895eef1-7870-4092-8bf9-c13f38b74173">MMC_TASK_DISPLAY_BITMAP</a>



<a href="https://msdn.microsoft.com/a46f1b86-883e-4eca-a3f8-d18c6a4d64e5">MMC_TASK_DISPLAY_SYMBOL</a>



<a href="https://msdn.microsoft.com/55d90530-5cd0-42ae-8a5d-417f7f49edac">MMC_TASK_DISPLAY_TYPE</a>
 

 

