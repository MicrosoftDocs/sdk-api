---
UID: NF:wingdi.GetAspectRatioFilterEx
title: GetAspectRatioFilterEx function (wingdi.h)
description: The GetAspectRatioFilterEx function retrieves the setting for the current aspect-ratio filter.
helpviewer_keywords: ["GetAspectRatioFilterEx","GetAspectRatioFilterEx function [Windows GDI]","_win32_GetAspectRatioFilterEx","gdi.getaspectratiofilterex","wingdi/GetAspectRatioFilterEx"]
old-location: gdi\getaspectratiofilterex.htm
tech.root: gdi
ms.assetid: 3f2dd47d-08bf-4848-897f-5ae506fba342
ms.date: 12/05/2018
ms.keywords: GetAspectRatioFilterEx, GetAspectRatioFilterEx function [Windows GDI], _win32_GetAspectRatioFilterEx, gdi.getaspectratiofilterex, wingdi/GetAspectRatioFilterEx
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetAspectRatioFilterEx
 - wingdi/GetAspectRatioFilterEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetAspectRatioFilterEx
---

# GetAspectRatioFilterEx function


## -description

The <b>GetAspectRatioFilterEx</b> function retrieves the setting for the current aspect-ratio filter.

## -parameters

### -param hdc [in]

Handle to a device context.

### -param lpsize [out]

Pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that receives the current aspect-ratio filter.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The aspect ratio is the ratio formed by the width and height of a pixel on a specified device.

The system provides a special filter, the aspect-ratio filter, to select fonts that were designed for a particular device. An application can specify that the system should only retrieve fonts matching the specified aspect ratio by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-setmapperflags">SetMapperFlags</a> function.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setmapperflags">SetMapperFlags</a>