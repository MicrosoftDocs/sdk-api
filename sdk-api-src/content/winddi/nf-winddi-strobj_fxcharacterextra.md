---
UID: NF:winddi.STROBJ_fxCharacterExtra
title: STROBJ_fxCharacterExtra function (winddi.h)
description: The STROBJ_fxCharacterExtra function retrieves the amount of extra space with which to augment each character's width in a string when displaying and/or printing it.
helpviewer_keywords: ["STROBJ_fxCharacterExtra","STROBJ_fxCharacterExtra function [Display Devices]","display.strobj_fxcharacterextra","gdifncs_4f8ab918-f3b4-47d8-9297-ae9e658f2bad.xml","winddi/STROBJ_fxCharacterExtra"]
old-location: display\strobj_fxcharacterextra.htm
tech.root: display
ms.assetid: 92989c16-5e82-4df2-9298-28b78757bd54
ms.date: 12/05/2018
ms.keywords: STROBJ_fxCharacterExtra, STROBJ_fxCharacterExtra function [Display Devices], display.strobj_fxcharacterextra, gdifncs_4f8ab918-f3b4-47d8-9297-ae9e658f2bad.xml, winddi/STROBJ_fxCharacterExtra
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
 - STROBJ_fxCharacterExtra
 - winddi/STROBJ_fxCharacterExtra
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
 - STROBJ_fxCharacterExtra
---

# STROBJ_fxCharacterExtra function


## -description

The <b>STROBJ_fxCharacterExtra</b> function retrieves the amount of extra space with which to augment each character's width in a string when displaying and/or printing it.

## -parameters

### -param pstro

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a> structure of the string to be displayed.

## -returns

<b>STROBJ_fxCharacterExtra</b> returns the amount of extra space to add to every character in the string. A return value of zero indicates that the string should be laid out using the characters' unaugmented widths.

## -remarks

The extra space value is specified in pixel coordinates.

<b>STROBJ_fxCharacterExtra</b> never fails.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-strobj_fxbreakextra">STROBJ_fxBreakExtra</a>