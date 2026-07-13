---
UID: NF:winddi.FONTOBJ_pwszFontFilePaths
title: FONTOBJ_pwszFontFilePaths function (winddi.h)
description: The FONTOBJ_pwszFontFilePaths function retrieves the file path(s) associated with a font.
helpviewer_keywords: ["FONTOBJ_pwszFontFilePaths","FONTOBJ_pwszFontFilePaths function [Display Devices]","display.fontobj_pwszfontfilepaths","gdifncs_51e9e4ce-3de8-4b6c-8d7f-ccd19b9bd449.xml","winddi/FONTOBJ_pwszFontFilePaths"]
old-location: display\fontobj_pwszfontfilepaths.htm
tech.root: display
ms.assetid: a175a282-4d0c-4379-b2f8-5e7e8cf7a137
ms.date: 12/05/2018
ms.keywords: FONTOBJ_pwszFontFilePaths, FONTOBJ_pwszFontFilePaths function [Display Devices], display.fontobj_pwszfontfilepaths, gdifncs_51e9e4ce-3de8-4b6c-8d7f-ccd19b9bd449.xml, winddi/FONTOBJ_pwszFontFilePaths
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FONTOBJ_pwszFontFilePaths
 - winddi/FONTOBJ_pwszFontFilePaths
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - FONTOBJ_pwszFontFilePaths
---

# FONTOBJ_pwszFontFilePaths function


## -description

The <b>FONTOBJ_pwszFontFilePaths</b> function retrieves the file path(s) associated with a font.

## -parameters

### -param pfo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure being queried.

### -param pcwc

Pointer to the location in which GDI returns the number of Unicode characters, including terminating zeros, found in all the returned font file path strings.

## -returns

<b>FONTOBJ_pwszFontFilePaths</b> returns a pointer to an array of font file path strings upon success. Each string is null terminated by a single Unicode zero. This function returns <b>NULL</b> upon failure or when the paths are not available for the specified font; that is, when the font is a temporary font added from a memory image.

## -remarks

Printer drivers can call <b>FONTOBJ_pwszFontFilePaths</b> when they want to do their own file mapping. File mapping is performed by calling <a href="/windows/desktop/api/winddi/nf-winddi-engmapfile">EngMapFile</a>.

Typically, there is only one file per font. For example, a TrueType font has only one file, whereas Type 1 fonts might require two files (a <i>.</i><a href="/windows-hardware/drivers/">pfm</a> and <i>.pfb</i>).

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engmapfile">EngMapFile</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>