---
UID: NF:winddi.DrvQueryAdvanceWidths
title: DrvQueryAdvanceWidths function (winddi.h)
description: The DrvQueryAdvanceWidths function returns character advance widths for a specified set of glyphs.
helpviewer_keywords: ["DrvQueryAdvanceWidths","DrvQueryAdvanceWidths function [Display Devices]","ddifncs_f97d4a54-b5e9-45b7-9d42-ece9073640a4.xml","display.drvqueryadvancewidths","winddi/DrvQueryAdvanceWidths"]
old-location: display\drvqueryadvancewidths.htm
tech.root: display
ms.assetid: b97114b5-6cc7-4af6-badb-d6aa5fc581ef
ms.date: 12/05/2018
ms.keywords: DrvQueryAdvanceWidths, DrvQueryAdvanceWidths function [Display Devices], ddifncs_f97d4a54-b5e9-45b7-9d42-ece9073640a4.xml, display.drvqueryadvancewidths, winddi/DrvQueryAdvanceWidths
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
 - DrvQueryAdvanceWidths
 - winddi/DrvQueryAdvanceWidths
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
 - DrvQueryAdvanceWidths
---

# DrvQueryAdvanceWidths function


## -description

The <b>DrvQueryAdvanceWidths</b> function returns character advance widths for a specified set of glyphs.

## -parameters

### -param dhpdev

Handle to the physical device's <a href="/windows-hardware/drivers/">PDEV</a> that was previously returned by <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>.

### -param pfo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure that identifies the font instance.

### -param iMode

Specifies the type of information to be provided. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
QAW_GETEASYWIDTHS

</td>
<td>
The character advance widths are returned as an array of 12.4 fixed-point numbers. This mode will not be used if the widths exceed the range of the 12.4 representation. This routine should compute widths as quickly as possible. If the computation of a glyph's character advance width cannot be accomplished efficiently, the driver should write 0xFFFF into the buffer for that glyph. The function returns DDI_ERROR if an error occurs, <b>FALSE</b> if not all widths can be efficiently computed for this mode, or <b>TRUE</b> in all other cases.

</td>
</tr>
<tr>
<td>
QAW_GETWIDTHS

</td>
<td>
The character advance widths are recorded as an array of 12.4 fixed-point numbers. This mode will not be used if the widths exceed the range of the 12.4 representation. The function returns <b>TRUE</b> if successful.

</td>
</tr>
</table>

### -param phg [in]

Pointer to an array of glyph handles that specify the glyphs for which the driver will return character advance widths.

### -param pvWidths [out]

Pointer to a buffer where the driver will record data.

### -param cGlyphs

Specifies the number of glyphs in the input buffer pointed to by <i>phg</i>.

## -returns

The return value is dependent on the value of the <i>iMode</i> parameter.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>