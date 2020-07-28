---
UID: NF:vfw.ICDecompressSetPalette
title: ICDecompressSetPalette macro (vfw.h)
description: The ICDecompressSetPalette macro specifies a palette for a video decompression driver to use if it is decompressing to a format that uses a palette. You can use this macro or explicitly call the ICM_DECOMPRESS_SET_PALETTE message.
helpviewer_keywords: ["ICDecompressSetPalette","ICDecompressSetPalette macro [Windows Multimedia]","_win32_ICDecompressSetPalette","multimedia.icdecompresssetpalette","vfw/ICDecompressSetPalette"]
old-location: multimedia\icdecompresssetpalette.htm
tech.root: Multimedia
ms.assetid: a3c4b04f-23a5-4499-b76e-50ab4565857d
ms.date: 12/05/2018
ms.keywords: ICDecompressSetPalette, ICDecompressSetPalette macro [Windows Multimedia], _win32_ICDecompressSetPalette, multimedia.icdecompresssetpalette, vfw/ICDecompressSetPalette
f1_keywords:
- vfw/ICDecompressSetPalette
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Vfw.h
api_name:
- ICDecompressSetPalette
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICDecompressSetPalette macro


## -description



The <b>ICDecompressSetPalette</b> macro specifies a palette for a video decompression driver to use if it is decompressing to a format that uses a palette. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompress-set-palette">ICM_DECOMPRESS_SET_PALETTE</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


### -param lpbiPalette

Pointer to a <a href="https://docs.microsoft.com/previous-versions/dd183376(v=vs.85)">BITMAPINFOHEADER</a> structure whose color table contains the colors that should be used if possible. You can specify zero to use the default set of output colors. 


## -remarks



This macro should not affect decompression already in progress; rather, colors passed using this message should be returned in response to future <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-icdecompressgetformat">ICDecompressGetFormat</a> and <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-icdecompressgetpalette">ICDecompressGetPalette</a> macros. Colors are sent back to the decompression driver in a future ICDecompressBegin macro.

This macro is used primarily when a driver decompresses images to the screen and another application that uses a palette is in the foreground, forcing the decompression driver to adapt to a foreign set of colors.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
 

 

