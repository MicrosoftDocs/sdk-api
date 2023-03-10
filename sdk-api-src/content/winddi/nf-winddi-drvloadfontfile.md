---
UID: NF:winddi.DrvLoadFontFile
title: DrvLoadFontFile function (winddi.h)
description: The DrvLoadFontFile function receives information from GDI relating to loading and mapping font files.
helpviewer_keywords: ["DrvLoadFontFile","DrvLoadFontFile function [Display Devices]","ddifncs_42238b28-ad71-4df8-b572-4ffd7ca2d3c1.xml","display.drvloadfontfile","winddi/DrvLoadFontFile"]
old-location: display\drvloadfontfile.htm
tech.root: display
ms.assetid: d9bcf8f8-40bc-48dc-85b7-67773c8a4ded
ms.date: 12/05/2018
ms.keywords: DrvLoadFontFile, DrvLoadFontFile function [Display Devices], ddifncs_42238b28-ad71-4df8-b572-4ffd7ca2d3c1.xml, display.drvloadfontfile, winddi/DrvLoadFontFile
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrvLoadFontFile
 - winddi/DrvLoadFontFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvLoadFontFile
---

# DrvLoadFontFile function


## -description

The <b>DrvLoadFontFile</b> function receives information from GDI relating to loading and mapping font files.

## -parameters

### -param cFiles

Caller-supplied value indicating the number of files associated with the font.

### -param piFile

Caller-supplied pointer to a <i>cFiles</i>-sized array of file handles. Each handle represents one of the files associated with the font. The file handles can be passed individually to <a href="/windows/desktop/api/winddi/nf-winddi-engmapfontfilefd">EngMapFontFileFD</a>.

### -param ppvView

Caller-supplied pointer to a <i>cFiles</i>-sized array containing the starting address of the memory space into which each font file has been mapped.

### -param pcjView

Caller-supplied pointer to a <i>cFiles</i>-sized array containing the size of the memory space into which each font file has been mapped.

### -param pdv

For Adobe Multiple Master fonts, this is a caller-supplied pointer to a DESIGNVECTOR structure (described in the Microsoft Windows SDK documentation) identifying the Multiple Master instance. Otherwise, this parameter is <b>NULL</b>.

### -param ulLangID

Caller-supplied language identifier, obtained from the registry.

### -param ulFastCheckSum

Specifies a GDI-supplied checksum for the font. If this parameter is nonzero, the GDI font cache engine can be used in order to access a font more quickly. If this parameter is zero, the GDI font engine cannot be used.

## -returns

If the operation succeeds, it should return a pointer to a driver-defined value that uniquely identifies the font. The driver subsequently receives this pointer as an input parameter to such functions as <a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfont">DrvQueryFont</a>, <a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfontfile">DrvQueryFontFile</a>, <a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfonttree">DrvQueryFontTree</a>. If an error is encountered, the function should return HFF_INVALID.

## -remarks

Font drivers are required to supply a <b>DrvLoadFontFile</b> function. The function's purpose is to allow a font driver to receive notification that a font's associated files are being loaded and mapped. The driver can store input arguments for later use.

Loading and mapping a font file entails calling <a href="/windows/desktop/api/winddi/nf-winddi-engmapfontfilefd">EngMapFontFileFD</a>. When an application calls <b>AddFontResource</b> or AddFontResourceEx (described in the Windows SDK documentation), GDI calls <b>EngMapFontFileFD</b> and then calls <b>DrvLoadFontFile</b>. The <b>DrvLoadFontFile</b> function's <i>ppvView</i> and <i>pcjView</i> parameters supply the location and size of each file's mapping, as returned by <b>EngMapFontFileFD</b>.

GDI unmaps the files when <b>DrvLoadFontFile</b> returns. If the driver needs to remap the files later, in response to subsequent calls from GDI, it can call <a href="/windows/desktop/api/winddi/nf-winddi-engmapfontfilefd">EngMapFontFileFD</a> itself if it has saved the <i>cFiles</i> and <i>piFile</i> parameters.

When the GDI font engine calls the font driver's <b>DrvLoadFontFile</b> DDI, it passes a checksum for the font in the <i>ulFastCheckSum</i>  parameter. If this parameter is nonzero and the font in question has been cached, <b>DrvLoadFontFile</b> can obtain a pointer to the font data with a call to <a href="/windows/desktop/api/winddi/nf-winddi-engfntcachelookup">EngFntCacheLookUp</a>. After the font driver obtains the pointer to the font data, it can then load the font data. If the font has not been cached, the font driver can cache the font by first allocating memory for the font cache, using a call to <a href="/windows/desktop/api/winddi/nf-winddi-engfntcachealloc">EngFntCacheAlloc</a>, and then writing the font data to that memory. If the font driver encounters an error reading or writing the font data, it can notify the GDI font engine by making a call to <a href="/windows/desktop/api/winddi/nf-winddi-engfntcachefault">EngFntCacheFault</a>.

If the GDI font engine called <b>DrvLoadFontFile</b> and passed in a value of zero for the <i>ulFastCheckSum</i> parameter, this means that the GDI font engine is not in operation, and the font driver does not need to take any action.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvunloadfontfile">DrvUnloadFontFile</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engfntcachealloc">EngFntCacheAlloc</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engfntcachefault">EngFntCacheFault</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engfntcachelookup">EngFntCacheLookUp</a>