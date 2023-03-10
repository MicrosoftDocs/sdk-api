---
UID: NF:winddi.DrvFontManagement
title: DrvFontManagement function (winddi.h)
description: The DrvFontManagement function is an optional entry point provided for PostScript devices.
helpviewer_keywords: ["DrvFontManagement","DrvFontManagement function [Display Devices]","ddifncs_d63b3833-8097-4fe0-b124-567aa07e917c.xml","display.drvfontmanagement","winddi/DrvFontManagement"]
old-location: display\drvfontmanagement.htm
tech.root: display
ms.assetid: cd52e32a-6d95-4aaf-96d3-45da2e5359e4
ms.date: 12/05/2018
ms.keywords: DrvFontManagement, DrvFontManagement function [Display Devices], ddifncs_d63b3833-8097-4fe0-b124-567aa07e917c.xml, display.drvfontmanagement, winddi/DrvFontManagement
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
 - DrvFontManagement
 - winddi/DrvFontManagement
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
 - DrvFontManagement
---

# DrvFontManagement function


## -description

The <b>DrvFontManagement</b> function is an optional entry point provided for PostScript devices.

## -parameters

### -param pso [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure.

### -param pfo [in, optional]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure.

### -param iMode [in]

Specifies the escape number to be performed. This must either be equal to QUERYESCSUPPORT (defined in <i>wingdi.h</i>), or in the range 0x100 through 0x3FE.

### -param cjIn [in]

Specifies the size, in bytes, of the buffer pointed to by the <i>pvIn</i> parameter.

### -param pvIn [in]

Pointer to an input buffer. If the <i>iMode</i> parameter is QUERYESCSUPPORT, <i>pvIn</i> points to a ULONG value in the range 0x100 through 0x3FE.

### -param cjOut [in]

Specifies the size, in bytes, of the output buffer pointed to by the <i>pvOut</i> parameter.

### -param pvOut [out]

Pointer to the output data buffer.

## -returns

If this function is hooked by the device driver then GDI will pass calls made by an application to <b>ExtEscape</b> for escape numbers 0x100 through 0x3fe, or for the QUERYESCSUPPORT escape when the first DWORD pointed to by <i>pvIn</i> is in the range 0x100 through 0x3fe.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>