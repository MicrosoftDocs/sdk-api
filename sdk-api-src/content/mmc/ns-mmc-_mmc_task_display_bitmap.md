---
UID: NS:mmc._MMC_TASK_DISPLAY_BITMAP
title: "_MMC_TASK_DISPLAY_BITMAP"
author: windows-sdk-content
description: The MMC_TASK_DISPLAY_BITMAP structure is introduced in MMC 1.1.
old-location: mmc\mmc_task_display_bitmap.htm
old-project: mmc
ms.assetid: 9895eef1-7870-4092-8bf9-c13f38b74173
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: MMC_TASK_DISPLAY_BITMAP, MMC_TASK_DISPLAY_BITMAP structure [MMC], _MMC_TASK_DISPLAY_BITMAP, _slate_mmc_task_display_bitmap, mmc.mmc_task_display_bitmap, mmc/MMC_TASK_DISPLAY_BITMAP
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: MMC_TASK_DISPLAY_BITMAP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_TASK_DISPLAY_BITMAP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MMC_TASK_DISPLAY_BITMAP structure


## -description


The 
<b>MMC_TASK_DISPLAY_BITMAP</b> structure is introduced in MMC 1.1.

The 
<b>MMC_TASK_DISPLAY_BITMAP</b> structure is used for the <b>uBitmap</b> member of the 
<a href="https://msdn.microsoft.com/ff43f0ea-2f33-4ed9-b5a5-484db2ffe3ad">MMC_TASK_DISPLAY_OBJECT</a> structure to specify all the data required to display a GIF or bitmap image for a task or background on a taskpad.


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



Allocate the <b>szMouseOverBitmap</b> and <b>szMouseOffBitmap</b> strings used in the structure with the COM API function <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> (or the equivalent) and MMC will release them.

If both <b>szMouseOverBitmap</b> and <b>szMouseOffBitmap</b> point to a <b>NULL</b> string, the task does not appear on the taskpad. If one of these strings is <b>NULL</b>, the other string is used for both.




## -see-also




<a href="https://msdn.microsoft.com/cb568307-7172-4941-a888-ff059f5256b6">IEnumTASK::Next</a>



<a href="https://msdn.microsoft.com/e34fc088-61d7-46a8-b493-8255a733d521">IExtendTaskPad::GetBackground</a>



<a href="https://msdn.microsoft.com/ff43f0ea-2f33-4ed9-b5a5-484db2ffe3ad">MMC_TASK_DISPLAY_OBJECT</a>



<a href="https://msdn.microsoft.com/a46f1b86-883e-4eca-a3f8-d18c6a4d64e5">MMC_TASK_DISPLAY_SYMBOL</a>



<a href="https://msdn.microsoft.com/55d90530-5cd0-42ae-8a5d-417f7f49edac">MMC_TASK_DISPLAY_TYPE</a>
 

 

