---
UID: NS:mmc._MMC_TASK_DISPLAY_SYMBOL
title: "_MMC_TASK_DISPLAY_SYMBOL"
author: windows-sdk-content
description: The MMC_TASK_DISPLAY_SYMBOL structure is introduced in MMC 1.1.
old-location: mmc\mmc_task_display_symbol.htm
old-project: MMC
ms.assetid: a46f1b86-883e-4eca-a3f8-d18c6a4d64e5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: MMC_TASK_DISPLAY_SYMBOL, MMC_TASK_DISPLAY_SYMBOL structure [MMC], _MMC_TASK_DISPLAY_SYMBOL, _slate_mmc_task_display_symbol, mmc.mmc_task_display_symbol, mmc/MMC_TASK_DISPLAY_SYMBOL
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
req.typenames: MMC_TASK_DISPLAY_SYMBOL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_TASK_DISPLAY_SYMBOL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MMC_TASK_DISPLAY_SYMBOL structure


## -description


The 
<b>MMC_TASK_DISPLAY_SYMBOL</b> structure is introduced in MMC 1.1.

The 
<b>MMC_TASK_DISPLAY_SYMBOL</b> structure is used for the <b>uSymbol</b> member of the 
<a href="https://msdn.microsoft.com/ff43f0ea-2f33-4ed9-b5a5-484db2ffe3ad">MMC_TASK_DISPLAY_OBJECT</a> structure to specify all the data required to display a symbol as an image for a task or background on a taskpad.


## -struct-fields




### -field szFontFamilyName

A pointer to a null-terminated string that contains the font family name of the symbol to display. 




For example, the following string specifies that the font is Webdings: "Webdings".

This should never be set to a <b>NULL</b> string or an empty string.


### -field szURLtoEOT

A pointer to a null-terminated string that contains the resource path to the EOT (embedded OpenType) file that contains the font for the symbol to display. 




The string should have the following form: "res://<i>filepath</i>/imgpath".

where <i>filepath</i> is the full path to the snap-in's DLL that stores the image file as a resource, and <i>imgpath</i> is the resource path of the image file with the snap-in DLL.

For example, the following string specifies that the snap-in DLL (snapin.dll) has a path of "c:\windows\system32\snapin.dll" and that the resource path is img/myfont.eot: "res://c:\\windows\\system32\\snapin.dll/img/myfont.eot".


### -field szSymbolString

A pointer to a null-terminated string that contains the character or characters to display in the symbol.


## -remarks



Allocate the <i>szFontFamilyName</i>, <i>szURLtoEOT</i>, and <i>szSymbolString</i> strings used in the structure with the COM API function <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> (or the equivalent) and MMC will release them.




## -see-also




<a href="https://msdn.microsoft.com/cb568307-7172-4941-a888-ff059f5256b6">IEnumTASK::Next</a>



<a href="https://msdn.microsoft.com/e34fc088-61d7-46a8-b493-8255a733d521">IExtendTaskPad::GetBackground</a>



<a href="https://msdn.microsoft.com/9895eef1-7870-4092-8bf9-c13f38b74173">MMC_TASK_DISPLAY_BITMAP</a>



<a href="https://msdn.microsoft.com/ff43f0ea-2f33-4ed9-b5a5-484db2ffe3ad">MMC_TASK_DISPLAY_OBJECT</a>



<a href="https://msdn.microsoft.com/55d90530-5cd0-42ae-8a5d-417f7f49edac">MMC_TASK_DISPLAY_TYPE</a>
 

 

