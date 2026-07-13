---
UID: NF:winddi.PALOBJ_cGetColors
title: PALOBJ_cGetColors function (winddi.h)
description: The PALOBJ_cGetColors function copies RGB colors from an indexed palette.
helpviewer_keywords: ["PALOBJ_cGetColors","PALOBJ_cGetColors function [Display Devices]","display.palobj_cgetcolors","gdifncs_b7181e52-6f68-4901-9d52-1791a973e6d6.xml","winddi/PALOBJ_cGetColors"]
old-location: display\palobj_cgetcolors.htm
tech.root: display
ms.assetid: c6bce32f-4daa-41e4-a495-8a3b56d70efc
ms.date: 12/05/2018
ms.keywords: PALOBJ_cGetColors, PALOBJ_cGetColors function [Display Devices], display.palobj_cgetcolors, gdifncs_b7181e52-6f68-4901-9d52-1791a973e6d6.xml, winddi/PALOBJ_cGetColors
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
 - PALOBJ_cGetColors
 - winddi/PALOBJ_cGetColors
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-common-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - PALOBJ_cGetColors
---

# PALOBJ_cGetColors function


## -description

The <b>PALOBJ_cGetColors</b> function copies RGB colors from an indexed palette.

## -parameters

### -param ppalo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-palobj">PALOBJ</a> structure that contains the RGB colors to be copied.

### -param iStart

Specifies the starting color index.

### -param cColors

Specifies the number of colors to be written.

### -param pulColors

Pointer to the buffer in which the colors are to be written.

## -returns

The return value is the number of colors written if the function is successful. Otherwise, it is zero.

## -remarks

A graphics driver can call this function in its implementation of <a href="/windows/desktop/api/winddi/nf-winddi-drvsetpalette">DrvSetPalette</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvsetpalette">DrvSetPalette</a>



<a href="/windows/desktop/api/winddi/ns-winddi-palobj">PALOBJ</a>