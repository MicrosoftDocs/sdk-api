---
UID: NF:vfw.ICDecompressGetFormat
title: ICDecompressGetFormat macro
author: windows-sdk-content
description: The ICDecompressGetFormat macro requests the output format of the decompressed data from a video decompression driver. You can use this macro or explicitly call the ICM_DECOMPRESS_GET_FORMAT message.
old-location: multimedia\icdecompressgetformat.htm
tech.root: Multimedia
ms.assetid: c45ff664-03f0-4cda-9ffd-fb7ea2656e43
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ICDecompressGetFormat, ICDecompressGetFormat macro [Windows Multimedia], _win32_ICDecompressGetFormat, multimedia.icdecompressgetformat, vfw/ICDecompressGetFormat
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
 - ICDecompressGetFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICDecompressGetFormat macro


## -description



The <b>ICDecompressGetFormat</b> macro requests the output format of the decompressed data from a video decompression driver. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/51753f47-758b-4d3e-9a53-9db284da2473">ICM_DECOMPRESS_GET_FORMAT</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


### -param lpbiInput

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure containing the input format. 


### -param lpbiOutput

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure to contain the output format. You can specify zero to request only the size of the output format, as in the <a href="https://msdn.microsoft.com/249a9d02-a51e-46f2-aea4-71460392705f">ICDecompressGetFormatSize</a> macro. 


## -remarks



If <i>lpbiOutput</i> is nonzero, the driver should fill the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure with the default output format corresponding to the input format specified for <i>lpbiInput</i>. If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

