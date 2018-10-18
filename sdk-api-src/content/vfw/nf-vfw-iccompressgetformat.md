---
UID: NF:vfw.ICCompressGetFormat
title: ICCompressGetFormat macro
author: windows-sdk-content
description: The ICCompressGetFormat macro requests the output format of the compressed data from a video compression driver. You can use this macro or explicitly call the ICM_COMPRESS_GET_FORMAT message.
old-location: multimedia\iccompressgetformat.htm
tech.root: Multimedia
ms.assetid: d6552dc0-21fb-475c-9ec4-cb3ef1f3a70e
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: ICCompressGetFormat, ICCompressGetFormat macro [Windows Multimedia], _win32_ICCompressGetFormat, multimedia.iccompressgetformat, vfw/ICCompressGetFormat
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

# ICCompressGetFormat macro


## -description



The <b>ICCompressGetFormat</b> macro requests the output format of the compressed data from a video compression driver. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/ac12d415-bad5-4838-b206-09c8097d3fd9">ICM_COMPRESS_GET_FORMAT</a> message.




## -parameters




### -param hic

Handle of the compressor. 


### -param lpbiInput

Pointer to a BITMAPINFO structure containing the input format.


### -param lpbiOutput

Pointer to a BITMAPINFO structure containing the output format. 


## -remarks



If <i>lpbiOutput</i> is nonzero, the driver should fill the <b>BITMAPINFO</b> structure with the default output format corresponding to the input format specified for <i>lpbiInput</i>. If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

