---
UID: NF:vfw.ICCompressGetFormatSize
title: ICCompressGetFormatSize macro
author: windows-sdk-content
description: The ICCompressGetFormatSize macro requests the size of the output format of the compressed data from a video compression driver. You can use this macro or explicitly call the ICM_COMPRESS_GET_FORMAT message.
old-location: multimedia\iccompressgetformatsize.htm
tech.root: Multimedia
ms.assetid: 50d73009-1f8e-4e2e-950c-0c1262ea61f0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICCompressGetFormatSize, ICCompressGetFormatSize macro [Windows Multimedia], _win32_ICCompressGetFormatSize, multimedia.iccompressgetformatsize, vfw/ICCompressGetFormatSize
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
 - ICCompressGetFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICCompressGetFormatSize macro


## -description



The <b>ICCompressGetFormatSize</b> macro requests the size of the output format of the compressed data from a video compression driver. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/ac12d415-bad5-4838-b206-09c8097d3fd9">ICM_COMPRESS_GET_FORMAT</a> message.




## -parameters




### -param hic

Handle of the compressor. 


### -param lpbi

Pointer to a <b>BITMAPINFO</b> structure containing the input format.


## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

