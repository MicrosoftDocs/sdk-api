---
UID: NF:winddi.FONTOBJ_pvTrueTypeFontFile
title: FONTOBJ_pvTrueTypeFontFile function (winddi.h)
description: The FONTOBJ_pvTrueTypeFontFile function retrieves a user-mode pointer to a view of a TrueType, OpenType, or Type1 font file.helpviewer_keywords: ["FONTOBJ_pvTrueTypeFontFile","FONTOBJ_pvTrueTypeFontFile function [Display Devices]","display.fontobj_pvtruetypefontfile","gdifncs_72ff6779-98e3-44b1-919c-06fa0ac1ffa2.xml","winddi/FONTOBJ_pvTrueTypeFontFile"]
old-location: display\fontobj_pvtruetypefontfile.htm
tech.root: display
ms.assetid: 2665d984-6a35-4950-92c0-82e7c8b633aa
ms.date: 12/05/2018
ms.keywords: FONTOBJ_pvTrueTypeFontFile, FONTOBJ_pvTrueTypeFontFile function [Display Devices], display.fontobj_pvtruetypefontfile, gdifncs_72ff6779-98e3-44b1-919c-06fa0ac1ffa2.xml, winddi/FONTOBJ_pvTrueTypeFontFile
f1_keywords:
- winddi/FONTOBJ_pvTrueTypeFontFile
dev_langs:
- c++
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
- FONTOBJ_pvTrueTypeFontFile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FONTOBJ_pvTrueTypeFontFile function


## -description


The <b>FONTOBJ_pvTrueTypeFontFile</b> function retrieves a user-mode pointer to a view of a TrueType, OpenType, or Type1 font file.


## -parameters




### -param pfo

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure with which the TrueType, PostScript OpenType, or PostScript Type1 font is associated.


### -param pcjFile

Pointer to a location in which GDI returns the size, in bytes, of the view of the font file.


## -returns



<b>FONTOBJ_pvTrueTypeFontFile</b> returns a pointer to a user-mode view of a font file upon success. If the FONTOBJ structure identifies a Type1 font, the return value is a pointer to the memory-mapped image of the <i>pfb</i> file. Otherwise, this function returns <b>NULL</b>.




## -remarks



<b>FONTOBJ_pvTrueTypeFontFile</b> should be called only for TrueType, OpenType, or Type1 fonts. The pointer returned by <b>FONTOBJ_pvTrueTypeFontFile</b> is valid only within the scope of the calling <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a> function. That is, the driver should not assume that the pointer returned by this function is valid upon exiting <i>DrvTextOut</i> and returning control to GDI.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>
 

 

