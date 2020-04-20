---
UID: NF:vfw.ICDecompressGetFormatSize
title: ICDecompressGetFormatSize macro (vfw.h)
description: The ICDecompressGetFormatSize macro requests the size of the output format of the decompressed data from a video decompression driver. You can use this macro or explicitly call the ICM_DECOMPRESS_GET_FORMAT message.helpviewer_keywords: ["ICDecompressGetFormatSize","ICDecompressGetFormatSize macro [Windows Multimedia]","_win32_ICDecompressGetFormatSize","multimedia.icdecompressgetformatsize","vfw/ICDecompressGetFormatSize"]
old-location: multimedia\icdecompressgetformatsize.htm
tech.root: Multimedia
ms.assetid: 249a9d02-a51e-46f2-aea4-71460392705f
ms.date: 12/05/2018
ms.keywords: ICDecompressGetFormatSize, ICDecompressGetFormatSize macro [Windows Multimedia], _win32_ICDecompressGetFormatSize, multimedia.icdecompressgetformatsize, vfw/ICDecompressGetFormatSize
f1_keywords:
- vfw/ICDecompressGetFormatSize
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
- ICDecompressGetFormatSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICDecompressGetFormatSize macro


## -description



The <b>ICDecompressGetFormatSize</b> macro requests the size of the output format of the decompressed data from a video decompression driver. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompress-get-format">ICM_DECOMPRESS_GET_FORMAT</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


### -param lpbi

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the input format. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
 

 

