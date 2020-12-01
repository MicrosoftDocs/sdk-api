---
UID: NF:winddi.DrvQueryTrueTypeTable
title: DrvQueryTrueTypeTable function (winddi.h)
description: The DrvQueryTrueTypeTable function accesses specific tables in a TrueType font-description file.
helpviewer_keywords: ["DrvQueryTrueTypeTable","DrvQueryTrueTypeTable function [Display Devices]","ddifncs_bcc0c4c9-b3f4-471d-8f04-1cca202e9d24.xml","display.drvquerytruetypetable","winddi/DrvQueryTrueTypeTable"]
old-location: display\drvquerytruetypetable.htm
tech.root: display
ms.assetid: d1c76df6-8c27-47b5-a879-4e064081481c
ms.date: 12/05/2018
ms.keywords: DrvQueryTrueTypeTable, DrvQueryTrueTypeTable function [Display Devices], ddifncs_bcc0c4c9-b3f4-471d-8f04-1cca202e9d24.xml, display.drvquerytruetypetable, winddi/DrvQueryTrueTypeTable
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
 - DrvQueryTrueTypeTable
 - winddi/DrvQueryTrueTypeTable
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
 - DrvQueryTrueTypeTable
---

# DrvQueryTrueTypeTable function


## -description

The <b>DrvQueryTrueTypeTable</b> function accesses specific tables in a TrueType font-description file.

## -parameters

### -param iFile

Pointer to a driver-defined value that identifies the driver-provided TrueType font file. This pointer is obtained from <a href="/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a>.

### -param ulFont

Specifies the one-based index of the driver font.

### -param ulTag

Specifies the table to access. If <i>ulTag</i> is zero, the driver should return access to the entire file.

### -param dpStart

Specifies the offset from the beginning of the tables from which to begin access. If <i>ulTag</i> is zero, <i>dpStart</i> is the offset from the beginning of the file.

### -param cjBuf

Specifies the size in bytes of the buffer to which <i>pjBuf</i> points, or zero.

### -param pjBuf

If not <b>NULL</b>, points to the buffer into which the driver should copy the table or font data.

### -param ppjTable

If not <b>NULL</b>, points to the location in which the driver should return the address of the table or font data.

### -param pcjTable

If not <b>NULL</b>, points to the location in which the driver should return the length in bytes of the table or font data to which *<i>ppjTable</i> points.

## -returns

<b>DrvQueryTrueTypeTable</b> returns one of the following values:

<ul>
<li>If <i>pjBuf</i> is <b>NULL</b>, the number of bytes required for the buffer to hold the entire table (this would be the same as the value returned in <i>pcjTable</i>). </li>
<li>If <i>pjBuf</i> is not <b>NULL</b>, the number of bytes copied. </li>
<li>If an error occurs, FD_ERROR. </li>
</ul>

## -remarks

<b>DrvQueryTrueTypeTable</b> must be implemented in TrueType font drivers.

There are two ways in which <b>DrvQueryTrueTypeTable</b> can be requested to return table or font data:

<ol>
<li>
When neither <i>cjBuf</i> nor <i>pjBuf</i> are <b>NULL</b>, the driver should copy the contents of the requested table into the buffer to which <i>pjBuf</i> points. In this situation, <i>ppjTable</i> and <i>pcjTable</i> will be <b>NULL</b> and should be ignored by the driver.

</li>
<li>
When neither <i>ppjTable</i> nor <i>pcjTable</i> are <b>NULL</b>, the driver should place a pointer to the table in *<i>ppjTable</i>, and the length, in bytes, of the table in *<i>pciTable</i>. In this situation, <i>cjBuf</i> and <i>pjBuf</i> will be <b>NULL</b> and should be ignored by the driver.

</li>
</ol>

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a>