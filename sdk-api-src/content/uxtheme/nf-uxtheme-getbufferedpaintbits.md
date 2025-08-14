---
UID: NF:uxtheme.GetBufferedPaintBits
title: GetBufferedPaintBits function (uxtheme.h)
description: Retrieves a pointer to the buffer bitmap if the buffer is a device-independent bitmap (DIB).
helpviewer_keywords: ["GetBufferedPaintBits","GetBufferedPaintBits function [Windows Controls]","_shell_GetBufferedPaintBits","_shell_GetBufferedPaintBits_cpp","controls.GetBufferedPaintBits","controls._shell_GetBufferedPaintBits","uxtheme/GetBufferedPaintBits"]
old-location: controls\GetBufferedPaintBits.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getbufferedpaintbits.htm
ms.date: 12/05/2018
ms.keywords: GetBufferedPaintBits, GetBufferedPaintBits function [Windows Controls], _shell_GetBufferedPaintBits, _shell_GetBufferedPaintBits_cpp, controls.GetBufferedPaintBits, controls._shell_GetBufferedPaintBits, uxtheme/GetBufferedPaintBits
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: UxTheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetBufferedPaintBits
 - uxtheme/GetBufferedPaintBits
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-uxtheme-themes-l1-1-3.dll
 - ext-ms-win-uxtheme-themes-l1-1-2.dll
 - UxTheme.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
 - xamlpalwp.dll
api_name:
 - GetBufferedPaintBits
---

# GetBufferedPaintBits function


## -description

Retrieves a pointer to the buffer bitmap if the buffer is a device-independent bitmap (DIB).

## -parameters

### -param hBufferedPaint

Type: <b>HPAINTBUFFER</b>

The handle of the buffered paint context, obtained through <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>.

### -param ppbBuffer [out]

Type: <b><a href="/windows/desktop/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>**</b>

When this function returns, contains a pointer to the address of the buffer bitmap pixels.

### -param pcxRow [out]

Type: <b>int*</b>

When this function returns, contains a pointer to the width, in pixels, of the buffer bitmap. This value is not necessarily equal to the buffer width. It may be larger.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful, or an error value otherwise. If an error occurs, <i>ppbBuffer</i>  is set to <b>NULL</b> and <i>pcxRow</i> is set to zero.

## -remarks

The number of bits per pixel depends on the pixel format passed to <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>.

## -see-also

<a href="/windows/desktop/api/uxtheme/ne-uxtheme-bp_bufferformat">BP_BUFFERFORMAT</a>



<a href="/windows/desktop/gdi/device-independent-bitmaps">Device-Independent Bitmaps</a>



<b>Other Resources</b>



<b>Reference</b>