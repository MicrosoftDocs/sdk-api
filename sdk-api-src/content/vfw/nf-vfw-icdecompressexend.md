---
UID: NF:vfw.ICDecompressExEnd
title: ICDecompressExEnd macro (vfw.h)
author: windows-sdk-content
description: The ICDecompressExEnd macro notifies a video decompression driver to end decompression and free resources allocated for decompression. You can use this macro or explicitly call the ICM_DECOMPRESSEX_END message.
old-location: multimedia\icdecompressexend.htm
tech.root: Multimedia
ms.assetid: db0ab881-2e26-4f60-a22c-cb4bd2016028
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICDecompressExEnd, ICDecompressExEnd macro [Windows Multimedia], _win32_ICDecompressExEnd, multimedia.icdecompressexend, vfw/ICDecompressExEnd
ms.topic: macro
f1_keywords: 
 - "vfw/ICDecompressExEnd"
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
 - ICDecompressExEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICDecompressExEnd macro


## -description



The <b>ICDecompressExEnd</b> macro notifies a video decompression driver to end decompression and free resources allocated for decompression. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompressex-end">ICM_DECOMPRESSEX_END</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


## -remarks



The driver frees any resources allocated for the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompressex-begin">ICM_DECOMPRESSEX_BEGIN</a> message.


<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-icdecompressexbegin">ICM_DECOMPRESSEX_BEGIN</a> and <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompressex-end">ICM_DECOMPRESSEX_END</a> do not nest. If your driver receives <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompressex-begin">ICM_DECOMPRESSEX_BEGIN</a> before decompression is stopped with <b>ICM_DECOMPRESSEX_END</b>, it should restart decompression with new parameters.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
 

 

