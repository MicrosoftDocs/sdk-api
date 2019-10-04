---
UID: NF:vfw.ICDecompressEnd
title: ICDecompressEnd macro (vfw.h)
author: windows-sdk-content
description: The ICDecompressEnd macro notifies a video decompression driver to end decompression and free resources allocated for decompression. You can use this macro or explicitly call the ICM_DECOMPRESS_END message.
old-location: multimedia\icdecompressend.htm
tech.root: Multimedia
ms.assetid: 9d66174a-b6bd-4bcd-a88a-bb1876bbc510
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICDecompressEnd, ICDecompressEnd macro [Windows Multimedia], _win32_ICDecompressEnd, multimedia.icdecompressend, vfw/ICDecompressEnd
ms.topic: macro
f1_keywords: 
 - "vfw/ICDecompressEnd"
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
 - ICDecompressEnd
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICDecompressEnd macro


## -description



The <b>ICDecompressEnd</b> macro notifies a video decompression driver to end decompression and free resources allocated for decompression. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompress-end">ICM_DECOMPRESS_END</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


## -remarks



The driver should free any resources allocated for the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompress-begin">ICM_DECOMPRESS_BEGIN</a> message.

The <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-icdecompressbegin">ICDecompressBegin</a> and <b>ICDecompressEnd</b> macros do not nest. If your driver receives <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompress-begin">ICM_DECOMPRESS_BEGIN</a> before decompression is stopped with <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompress-end">ICM_DECOMPRESS_END</a>, it should restart decompression with new parameters.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
 

 

