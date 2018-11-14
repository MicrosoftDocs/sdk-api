---
UID: NF:winddi.FONTOBJ_pwszFontFilePaths
title: FONTOBJ_pwszFontFilePaths function
author: windows-sdk-content
description: The FONTOBJ_pwszFontFilePaths function retrieves the file path(s) associated with a font.
old-location: display\fontobj_pwszfontfilepaths.htm
tech.root: display
ms.assetid: a175a282-4d0c-4379-b2f8-5e7e8cf7a137
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: FONTOBJ_pwszFontFilePaths, FONTOBJ_pwszFontFilePaths function [Display Devices], display.fontobj_pwszfontfilepaths, gdifncs_51e9e4ce-3de8-4b6c-8d7f-ccd19b9bd449.xml, winddi/FONTOBJ_pwszFontFilePaths
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - FONTOBJ_pwszFontFilePaths
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- FONTOBJ_pwszFontFilePaths
: 
---

# FONTOBJ_pwszFontFilePaths function


## -description


The <b>FONTOBJ_pwszFontFilePaths</b> function retrieves the file path(s) associated with a font.


## -parameters




### -param pfo

Pointer to the <a href="https://msdn.microsoft.com/09af2006-51f1-433e-9227-3c99b9860e75">FONTOBJ</a> structure being queried.


### -param pcwc

Pointer to the location in which GDI returns the number of Unicode characters, including terminating zeros, found in all the returned font file path strings.


## -returns



<b>FONTOBJ_pwszFontFilePaths</b> returns a pointer to an array of font file path strings upon success. Each string is null terminated by a single Unicode zero. This function returns <b>NULL</b> upon failure or when the paths are not available for the specified font; that is, when the font is a temporary font added from a memory image.




## -remarks



Printer drivers can call <b>FONTOBJ_pwszFontFilePaths</b> when they want to do their own file mapping. File mapping is performed by calling <a href="https://msdn.microsoft.com/6887f7e1-f94f-421c-be7a-14a41d621ce1">EngMapFile</a>.

Typically, there is only one file per font. For example, a TrueType font has only one file, whereas Type 1 fonts might require two files (a <i>.</i><a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">pfm</a> and <i>.pfb</i>).




## -see-also




<a href="https://msdn.microsoft.com/6887f7e1-f94f-421c-be7a-14a41d621ce1">EngMapFile</a>



<a href="https://msdn.microsoft.com/09af2006-51f1-433e-9227-3c99b9860e75">FONTOBJ</a>
 

 

