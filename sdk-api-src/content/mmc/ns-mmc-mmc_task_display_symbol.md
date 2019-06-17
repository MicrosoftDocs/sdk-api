---
UID: NS:mmc._MMC_TASK_DISPLAY_SYMBOL
title: MMC_TASK_DISPLAY_SYMBOL (mmc.h)
author: windows-sdk-content
description: The MMC_TASK_DISPLAY_SYMBOL structure is introduced in MMC 1.1.
old-location: mmc\mmc_task_display_symbol.htm
tech.root: mmc
ms.assetid: a46f1b86-883e-4eca-a3f8-d18c6a4d64e5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MMC_TASK_DISPLAY_SYMBOL, MMC_TASK_DISPLAY_SYMBOL structure [MMC], _slate_mmc_task_display_symbol, mmc.mmc_task_display_symbol, mmc/MMC_TASK_DISPLAY_SYMBOL
ms.topic: struct
f1_keywords: ["mmc/MMC_TASK_DISPLAY_SYMBOL"]
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
 - MMC_TASK_DISPLAY_SYMBOL
product: Windows
targetos: Windows
req.typenames: MMC_TASK_DISPLAY_SYMBOL
req.redist: 
ms.custom: 19H1
---

# MMC_TASK_DISPLAY_SYMBOL structure


## -description


The 
<b>MMC_TASK_DISPLAY_SYMBOL</b> structure is introduced in MMC 1.1.

The 
<b>MMC_TASK_DISPLAY_SYMBOL</b> structure is used for the <b>uSymbol</b> member of the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/ns-mmc-_mmc_task_display_object">MMC_TASK_DISPLAY_OBJECT</a> structure to specify all the data required to display a symbol as an image for a task or background on a taskpad.


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



Allocate the <i>szFontFamilyName</i>, <i>szURLtoEOT</i>, and <i>szSymbolString</i> strings used in the structure with the COM API function <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> (or the equivalent) and MMC will release them.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-ienumtask-next">IEnumTASK::Next</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-getbackground">IExtendTaskPad::GetBackground</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/ns-mmc-_mmc_task_display_bitmap">MMC_TASK_DISPLAY_BITMAP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/ns-mmc-_mmc_task_display_object">MMC_TASK_DISPLAY_OBJECT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/ne-mmc-_mmc_task_display_type">MMC_TASK_DISPLAY_TYPE</a>
 

 

