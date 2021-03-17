---
UID: NF:wingdi.GetRasterizerCaps
title: GetRasterizerCaps function (wingdi.h)
description: The GetRasterizerCaps function returns flags indicating whether TrueType fonts are installed in the system.
helpviewer_keywords: ["GetRasterizerCaps","GetRasterizerCaps function [Windows GDI]","_win32_GetRasterizerCaps","gdi.getrasterizercaps","wingdi/GetRasterizerCaps"]
old-location: gdi\getrasterizercaps.htm
tech.root: gdi
ms.assetid: 0898d1c0-5480-4bd2-aa45-918340172a05
ms.date: 12/05/2018
ms.keywords: GetRasterizerCaps, GetRasterizerCaps function [Windows GDI], _win32_GetRasterizerCaps, gdi.getrasterizercaps, wingdi/GetRasterizerCaps
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
 - GetRasterizerCaps
 - wingdi/GetRasterizerCaps
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
 - GetRasterizerCaps
---

# GetRasterizerCaps function


## -description

The <b>GetRasterizerCaps</b> function returns flags indicating whether TrueType fonts are installed in the system.

## -parameters

### -param lpraststat [out]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-rasterizer_status">RASTERIZER_STATUS</a> structure that receives information about the rasterizer.

### -param cjBytes [in]

The number of bytes to be copied into the structure pointed to by the <i>lprs</i> parameter.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>GetRasterizerCaps</b> function enables applications and printer drivers to determine whether TrueType fonts are installed.

If the TT_AVAILABLE flag is set in the <b>wFlags</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-rasterizer_status">RASTERIZER_STATUS</a> structure, at least one TrueType font is installed. If the TT_ENABLED flag is set, TrueType is enabled for the system.

The actual number of bytes copied is either the member specified in the <i>cb</i> parameter or the length of the <a href="/windows/desktop/api/wingdi/ns-wingdi-rasterizer_status">RASTERIZER_STATUS</a> structure, whichever is less.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getoutlinetextmetricsa">GetOutlineTextMetrics</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-rasterizer_status">RASTERIZER_STATUS</a>