---
UID: NF:vfw.ICDecompressQuery
title: ICDecompressQuery macro (vfw.h)
author: windows-sdk-content
description: The ICDecompressQuery macro queries a video decompression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.
old-location: multimedia\icdecompressquery.htm
tech.root: Multimedia
ms.assetid: 77d9a28c-dff9-4ccb-a0b8-9dc38fc66372
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICDecompressQuery, ICDecompressQuery macro [Windows Multimedia], _win32_ICDecompressQuery, multimedia.icdecompressquery, vfw/ICDecompressQuery
ms.topic: macro
f1_keywords: 
 - "vfw/ICDecompressQuery"
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
 - ICDecompressQuery
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICDecompressQuery macro


## -description



The <b>ICDecompressQuery</b> macro queries a video decompression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-decompress-query">ICM_DECOMPRESS_QUERY</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


### -param lpbiInput

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the input format. 


### -param lpbiOutput

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the output format. You can specify zero for this parameter to indicate any output format is acceptable. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
 

 

