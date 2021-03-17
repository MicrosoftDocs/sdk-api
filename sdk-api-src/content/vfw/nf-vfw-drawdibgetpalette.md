---
UID: NF:vfw.DrawDibGetPalette
title: DrawDibGetPalette function (vfw.h)
description: The DrawDibGetPalette function retrieves the palette used by a DrawDib DC.
helpviewer_keywords: ["DrawDibGetPalette","DrawDibGetPalette function [Windows Multimedia]","_win32_DrawDibGetPalette","multimedia.drawdibgetpalette","vfw/DrawDibGetPalette"]
old-location: multimedia\drawdibgetpalette.htm
tech.root: Multimedia
ms.assetid: 38ed99a7-f704-467b-a23f-a19c990d0b10
ms.date: 12/05/2018
ms.keywords: DrawDibGetPalette, DrawDibGetPalette function [Windows Multimedia], _win32_DrawDibGetPalette, multimedia.drawdibgetpalette, vfw/DrawDibGetPalette
req.header: vfw.h
req.include-header: 
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
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawDibGetPalette
 - vfw/DrawDibGetPalette
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - DrawDibGetPalette
---

# DrawDibGetPalette function


## -description

The <b>DrawDibGetPalette</b> function retrieves the palette used by a DrawDib DC.

## -parameters

### -param hdd

Handle to a DrawDib DC.

## -returns

Returns a handle to the palette if successful or <b>NULL</b> otherwise.

## -remarks

This function assumes the DrawDib DC contains a valid palette entry, implying that a call to this function must follow calls to the <a href="/windows/desktop/api/vfw/nf-vfw-drawdibdraw">DrawDibDraw</a> or <a href="/windows/desktop/api/vfw/nf-vfw-drawdibbegin">DrawDibBegin</a> functions.

You should rarely need to call this function because you can realize the correct palette in response to a window message by using the <a href="/windows/desktop/api/vfw/nf-vfw-drawdibrealize">DrawDibRealize</a> function.

## -see-also

<a href="/windows/desktop/Multimedia/drawdib-functions">DrawDib Functions</a>