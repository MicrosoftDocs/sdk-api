---
UID: NF:vfw.ICDecompressGetPalette
title: ICDecompressGetPalette macro (vfw.h)
author: windows-sdk-content
description: The ICDecompressGetPalette macro requests that the video decompression driver supply the color table of the output BITMAPINFOHEADER structure. You can use this macro or explicitly call the ICM_DECOMPRESS_GET_PALETTE message.
old-location: multimedia\icdecompressgetpalette.htm
tech.root: Multimedia
ms.assetid: 433155ce-f9a1-408d-9caa-43a736fbdc67
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICDecompressGetPalette, ICDecompressGetPalette macro [Windows Multimedia], _win32_ICDecompressGetPalette, multimedia.icdecompressgetpalette, vfw/ICDecompressGetPalette
ms.topic: macro
f1_keywords: 
 - "vfw/ICDecompressGetPalette"
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
 - ICDecompressGetPalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICDecompressGetPalette macro


## -description



The <b>ICDecompressGetPalette</b> macro requests that the video decompression driver supply the color table of the output <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfoheader">BITMAPINFOHEADER</a> structure. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompress-get-palette">ICM_DECOMPRESS_GET_PALETTE</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


### -param lpbiInput

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfoheader">BITMAPINFOHEADER</a> structure containing the input format. 


### -param lpbiOutput

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfoheader">BITMAPINFOHEADER</a> structure to contain the color table. The space reserved for the color table is always at least 256 colors. You can specify zero for this parameter to return only the size of the color table. 


## -remarks



If <i>lpbiOutput</i> is nonzero, the driver sets the <b>biClrUsed</b> member of <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfoheader">BITMAPINFOHEADER</a> to the number of colors in the color table. The driver fills the <b>bmiColors</b> members of <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfo">BITMAPINFO</a> with the actual colors.

The driver should support this message only if it uses a palette other than the one specified in the input format.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
 

 

