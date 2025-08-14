---
UID: NF:winddi.EngGetCurrentCodePage
title: EngGetCurrentCodePage function (winddi.h)
description: The EngGetCurrentCodePage function returns the system's default OEM and ANSI code pages.
helpviewer_keywords: ["EngGetCurrentCodePage","EngGetCurrentCodePage function [Display Devices]","display.enggetcurrentcodepage","gdifncs_39440cc8-e1f5-4f88-b92a-d8a7eb3d1d39.xml","winddi/EngGetCurrentCodePage"]
old-location: display\enggetcurrentcodepage.htm
tech.root: display
ms.assetid: d53a1b6b-40b1-42a5-acfe-4b17f24d00c1
ms.date: 12/05/2018
ms.keywords: EngGetCurrentCodePage, EngGetCurrentCodePage function [Display Devices], display.enggetcurrentcodepage, gdifncs_39440cc8-e1f5-4f88-b92a-d8a7eb3d1d39.xml, winddi/EngGetCurrentCodePage
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
 - EngGetCurrentCodePage
 - winddi/EngGetCurrentCodePage
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngGetCurrentCodePage
---

# EngGetCurrentCodePage function


## -description

The <b>EngGetCurrentCodePage</b> function returns the system's default OEM and ANSI code pages.

## -parameters

### -param OemCodePage [out]

Pointer to a USHORT that receives the system's default OEM code page.

### -param AnsiCodePage [out]

Pointer to a USHORT that receives the system's default ANSI code page.

## -returns

None

## -remarks

<b>EngGetCurrentCodePage</b> returns the default code pages that are used by the system to translate from ANSI to Unicode. These values are set at boot time according to locale settings.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-strobj_dwgetcodepage">STROBJ_dwGetCodePage</a>