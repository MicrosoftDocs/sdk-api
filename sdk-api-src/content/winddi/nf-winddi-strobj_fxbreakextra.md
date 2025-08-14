---
UID: NF:winddi.STROBJ_fxBreakExtra
title: STROBJ_fxBreakExtra function (winddi.h)
description: The STROBJ_fxBreakExtra function retrieves the amount of extra space to be added to each space character in a string when displaying and/or printing justified text.
helpviewer_keywords: ["STROBJ_fxBreakExtra","STROBJ_fxBreakExtra function [Display Devices]","display.strobj_fxbreakextra","gdifncs_cfaecb83-e351-447e-ba9d-63ef6dc3f4d8.xml","winddi/STROBJ_fxBreakExtra"]
old-location: display\strobj_fxbreakextra.htm
tech.root: display
ms.assetid: 857068ab-2c47-402b-a64a-691bdc52a298
ms.date: 12/05/2018
ms.keywords: STROBJ_fxBreakExtra, STROBJ_fxBreakExtra function [Display Devices], display.strobj_fxbreakextra, gdifncs_cfaecb83-e351-447e-ba9d-63ef6dc3f4d8.xml, winddi/STROBJ_fxBreakExtra
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
 - STROBJ_fxBreakExtra
 - winddi/STROBJ_fxBreakExtra
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
 - STROBJ_fxBreakExtra
---

# STROBJ_fxBreakExtra function


## -description

The <b>STROBJ_fxBreakExtra</b> function retrieves the amount of extra space to be added to each space character in a string when displaying and/or printing justified text.

## -parameters

### -param pstro

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a> structure of the string to be displayed.

## -returns

<b>STROBJ_fxBreakExtra</b> returns the amount of extra space to add to each space character in the string. A return value of zero indicates that no extra space is added to space characters in a string.

## -remarks

The extra space value is specified in pixel coordinates.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-strobj_fxcharacterextra">STROBJ_fxCharacterExtra</a>