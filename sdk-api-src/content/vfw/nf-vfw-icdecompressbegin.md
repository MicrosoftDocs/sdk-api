---
UID: NF:vfw.ICDecompressBegin
title: ICDecompressBegin macro (vfw.h)
description: The ICDecompressBegin macro notifies a video decompression driver to prepare to decompress data. You can use this macro or explicitly call the ICM_DECOMPRESS_BEGIN message.helpviewer_keywords: ["ICDecompressBegin","ICDecompressBegin macro [Windows Multimedia]","_win32_ICDecompressBegin","multimedia.icdecompressbegin","vfw/ICDecompressBegin"]
old-location: multimedia\icdecompressbegin.htm
tech.root: Multimedia
ms.assetid: 3e9fb4b7-bdc6-402c-a5c6-3f837149c291
ms.date: 12/05/2018
ms.keywords: ICDecompressBegin, ICDecompressBegin macro [Windows Multimedia], _win32_ICDecompressBegin, multimedia.icdecompressbegin, vfw/ICDecompressBegin
f1_keywords:
- vfw/ICDecompressBegin
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
- ICDecompressBegin
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICDecompressBegin macro


## -description



The <b>ICDecompressBegin</b> macro notifies a video decompression driver to prepare to decompress data. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompress-begin">ICM_DECOMPRESS_BEGIN</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


### -param lpbiInput

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the input format. 


### -param lpbiOutput

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the output format. 


## -remarks



When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompress">ICM_DECOMPRESS</a> messages efficiently.

The <b>ICDecompressBegin</b> and <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-icdecompressend">ICDecompressEnd</a> macros do not nest. If your driver receives <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompress-begin">ICM_DECOMPRESS_BEGIN</a> before decompression is stopped with <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompress-end">ICM_DECOMPRESS_END</a>, it should restart decompression with new parameters.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
 

 

