---
UID: NF:winddi.EngEraseSurface
title: EngEraseSurface function (winddi.h)
description: The EngEraseSurface function calls GDI to erase the surface; a given rectangle on the surface will be filled with the given color.
helpviewer_keywords: ["EngEraseSurface","EngEraseSurface function [Display Devices]","display.engerasesurface","gdifncs_49673ad2-d8a0-4c8b-bf0f-c1fab9f3c519.xml","winddi/EngEraseSurface"]
old-location: display\engerasesurface.htm
tech.root: display
ms.assetid: 3dace2e1-2a6b-42e5-a556-a3952cf4786c
ms.date: 12/05/2018
ms.keywords: EngEraseSurface, EngEraseSurface function [Display Devices], display.engerasesurface, gdifncs_49673ad2-d8a0-4c8b-bf0f-c1fab9f3c519.xml, winddi/EngEraseSurface
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
 - EngEraseSurface
 - winddi/EngEraseSurface
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
 - EngEraseSurface
---

# EngEraseSurface function


## -description

The <b>EngEraseSurface</b> function calls GDI to erase the surface; a given rectangle on the surface will be filled with the given color.

## -parameters

### -param pso

Pointer to the surface to erase.

### -param prcl

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that defines which pixels to erase on the surface. This rectangle is exclusive of the bottom and right edges.

### -param iColor [in]

Specifies a color index. This is an index to the value that will be written into each pixel.

## -returns

The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is reported.