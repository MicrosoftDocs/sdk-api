---
UID: NF:vfw.ICCompressQuery
title: ICCompressQuery macro (vfw.h)
description: The ICCompressQuery macro queries a video compression driver to determine if it supports a specific input format or if it can compress a specific input format to a specific output format.helpviewer_keywords: ["ICCompressQuery","ICCompressQuery macro [Windows Multimedia]","_win32_ICCompressQuery","multimedia.iccompressquery","vfw/ICCompressQuery"]
old-location: multimedia\iccompressquery.htm
tech.root: Multimedia
ms.assetid: 5e34a830-5e0c-41e5-9e4a-2d827c73ceeb
ms.date: 12/05/2018
ms.keywords: ICCompressQuery, ICCompressQuery macro [Windows Multimedia], _win32_ICCompressQuery, multimedia.iccompressquery, vfw/ICCompressQuery
f1_keywords:
- vfw/ICCompressQuery
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
- ICCompressQuery
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICCompressQuery macro


## -description



The <b>ICCompressQuery</b> macro queries a video compression driver to determine if it supports a specific input format or if it can compress a specific input format to a specific output format. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-compress-query">ICM_COMPRESS_QUERY</a> message.




## -parameters




### -param hic

Handle to a compressor. 


### -param lpbiInput

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the input format. 


### -param lpbiOutput

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the output format. You can specify zero for this parameter to indicate any output format is acceptable. 


## -remarks



When a driver receives this message, it should examine the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure associated with <i>lpbiInput</i> to determine if it can compress the input format.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
 

 

