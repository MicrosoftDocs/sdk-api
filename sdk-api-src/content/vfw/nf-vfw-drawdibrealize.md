---
UID: NF:vfw.DrawDibRealize
title: DrawDibRealize function (vfw.h)
description: The DrawDibRealize function realizes the palette of the DrawDib DC for use with the specified DC.
helpviewer_keywords: ["DrawDibRealize","DrawDibRealize function [Windows Multimedia]","_win32_DrawDibRealize","multimedia.drawdibrealize","vfw/DrawDibRealize"]
old-location: multimedia\drawdibrealize.htm
tech.root: Multimedia
ms.assetid: 4723c8a4-36af-4543-b6df-d51f68a3e94d
ms.date: 12/05/2018
ms.keywords: DrawDibRealize, DrawDibRealize function [Windows Multimedia], _win32_DrawDibRealize, multimedia.drawdibrealize, vfw/DrawDibRealize
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
 - DrawDibRealize
 - vfw/DrawDibRealize
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
 - DrawDibRealize
---

# DrawDibRealize function


## -description

The <b>DrawDibRealize</b> function realizes the palette of the DrawDib DC for use with the specified DC.

## -parameters

### -param hdd

Handle to a DrawDib DC.

### -param hdc

Handle to the DC containing the palette.

### -param fBackground

Background palette flag. If this value is nonzero, the palette is a background palette. If this value is zero and the DC is attached to a window, the logical palette becomes the foreground palette when the window has the input focus. (A DC is attached to a window when the window class style is CS_OWNDC or when the DC is obtained by using the <a href="/previous-versions//ms533241(v=vs.85)">GetDC</a> function.)

## -returns

Returns the number of entries in the logical palette mapped to different values in the system palette. If an error occurs or no colors were updated, it returns zero.

## -remarks

To select the palette of the DrawDib DC as a background palette, use the <a href="/windows/desktop/api/vfw/nf-vfw-drawdibdraw">DrawDibDraw</a> function and specify the DDF_BACKGROUNDPAL flag.

## -see-also

<a href="/windows/desktop/Multimedia/drawdib-functions">DrawDib Functions</a>