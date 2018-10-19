---
UID: NF:vfw.ICDecompressGetFormatSize
title: ICDecompressGetFormatSize macro
author: windows-sdk-content
description: The ICDecompressGetFormatSize macro requests the size of the output format of the decompressed data from a video decompression driver. You can use this macro or explicitly call the ICM_DECOMPRESS_GET_FORMAT message.
old-location: multimedia\icdecompressgetformatsize.htm
tech.root: Multimedia
ms.assetid: 249a9d02-a51e-46f2-aea4-71460392705f
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ICDecompressGetFormatSize, ICDecompressGetFormatSize macro [Windows Multimedia], _win32_ICDecompressGetFormatSize, multimedia.icdecompressgetformatsize, vfw/ICDecompressGetFormatSize
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
 - ICDecompressGetFormatSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICDecompressGetFormatSize macro


## -description



The <b>ICDecompressGetFormatSize</b> macro requests the size of the output format of the decompressed data from a video decompression driver. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/51753f47-758b-4d3e-9a53-9db284da2473">ICM_DECOMPRESS_GET_FORMAT</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


### -param lpbi

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure containing the input format. 


## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

