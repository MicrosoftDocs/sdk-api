---
UID: NF:vfw.ICDecompressSetPalette
title: ICDecompressSetPalette macro
author: windows-sdk-content
description: The ICDecompressSetPalette macro specifies a palette for a video decompression driver to use if it is decompressing to a format that uses a palette. You can use this macro or explicitly call the ICM_DECOMPRESS_SET_PALETTE message.
old-location: multimedia\icdecompresssetpalette.htm
tech.root: Multimedia
ms.assetid: a3c4b04f-23a5-4499-b76e-50ab4565857d
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ICDecompressSetPalette, ICDecompressSetPalette macro [Windows Multimedia], _win32_ICDecompressSetPalette, multimedia.icdecompresssetpalette, vfw/ICDecompressSetPalette
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICDecompressSetPalette macro


## -description



The <b>ICDecompressSetPalette</b> macro specifies a palette for a video decompression driver to use if it is decompressing to a format that uses a palette. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/269d01f9-b7c8-40e4-abdb-24dd0c9cc18d">ICM_DECOMPRESS_SET_PALETTE</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


### -param lpbiPalette

Pointer to a <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a> structure whose color table contains the colors that should be used if possible. You can specify zero to use the default set of output colors. 


## -remarks



This macro should not affect decompression already in progress; rather, colors passed using this message should be returned in response to future <a href="https://msdn.microsoft.com/c45ff664-03f0-4cda-9ffd-fb7ea2656e43">ICDecompressGetFormat</a> and <a href="https://msdn.microsoft.com/433155ce-f9a1-408d-9caa-43a736fbdc67">ICDecompressGetPalette</a> macros. Colors are sent back to the decompression driver in a future ICDecompressBegin macro.

This macro is used primarily when a driver decompresses images to the screen and another application that uses a palette is in the foreground, forcing the decompression driver to adapt to a foreign set of colors.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

