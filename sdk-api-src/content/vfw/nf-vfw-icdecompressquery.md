---
UID: NF:vfw.ICDecompressQuery
title: ICDecompressQuery macro
author: windows-sdk-content
description: The ICDecompressQuery macro queries a video decompression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.
old-location: multimedia\icdecompressquery.htm
old-project: Multimedia
ms.assetid: 77d9a28c-dff9-4ccb-a0b8-9dc38fc66372
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICDecompressQuery, ICDecompressQuery macro [Windows Multimedia], _win32_ICDecompressQuery, multimedia.icdecompressquery, vfw/ICDecompressQuery
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: vfw.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICDecompressQuery
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICDecompressQuery macro


## -description



The <b>ICDecompressQuery</b> macro queries a video decompression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/622dd1de-3f7a-4841-913c-282c2ad766f4">ICM_DECOMPRESS_QUERY</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


### -param lpbiInput

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure containing the input format. 


### -param lpbiOutput

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure containing the output format. You can specify zero for this parameter to indicate any output format is acceptable. 


## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

