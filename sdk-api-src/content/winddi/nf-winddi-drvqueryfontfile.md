---
UID: NF:winddi.DrvQueryFontFile
title: DrvQueryFontFile function (winddi.h)
description: The DrvQueryFontFile function provides font file information.
helpviewer_keywords: ["DrvQueryFontFile","DrvQueryFontFile function [Display Devices]","ddifncs_e1440df7-d91a-4c86-b43b-10a5c5b7aab9.xml","display.drvqueryfontfile","winddi/DrvQueryFontFile"]
old-location: display\drvqueryfontfile.htm
tech.root: display
ms.assetid: 4d853dbd-0448-43c3-9f01-13b7118a0743
ms.date: 12/05/2018
ms.keywords: DrvQueryFontFile, DrvQueryFontFile function [Display Devices], ddifncs_e1440df7-d91a-4c86-b43b-10a5c5b7aab9.xml, display.drvqueryfontfile, winddi/DrvQueryFontFile
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
 - DrvQueryFontFile
 - winddi/DrvQueryFontFile
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
 - DrvQueryFontFile
---

# DrvQueryFontFile function


## -description

The <b>DrvQueryFontFile</b> function provides font file information.

## -parameters

### -param iFile

Pointer to a driver-defined value that identifies the driver font file. This pointer is returned by a prior call to <a href="/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a>.

### -param ulMode

Specifies the type of information to be written. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
QFF_DESCRIPTION

</td>
<td>
The function provides a string that an NT-based operating system will use to describe the font file. A null-terminated Unicode string is written to the buffer pointed to by <i>pulBuffer</i>.

</td>
</tr>
<tr>
<td>
QFF_NUMFACES

</td>
<td>
The function returns the number of typefaces in the font file; the <i>cjBuf</i> and <i>pulBuf</i> parameters are ignored. Typefaces are identified by an index ranging from one through the number of typefaces.

</td>
</tr>
</table>

### -param cjBuf

Specifies the size, in bytes, of the return buffer.

### -param pulBuf

Pointer to the return buffer.

## -returns

If <i>ulMode</i> is QFF_NUMFACES, then the return value is the number of faces in the font file. If <i>pulBuf</i> is <b>NULL</b>, it is the number of bytes of data that would be written to <i>pulBuf</i>; otherwise, it is the number of bytes written to <i>pulBuf</i>. If an error occurs, the return value is FD_ERROR.

## -remarks

<b>DrvQueryFontFile</b> is required for font drivers.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a>