---
UID: NF:vfw.ICCompressGetSize
title: ICCompressGetSize macro
author: windows-sdk-content
description: The ICCompressGetSize macro requests that the video compression driver supply the maximum size of one frame of data when compressed into the specified output format. You can use this macro or explicitly call the ICM_COMPRESS_GET_SIZE message.
old-location: multimedia\iccompressgetsize.htm
old-project: Multimedia
ms.assetid: 6cb85b0b-4a05-44f7-af61-303a94b49847
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ICCompressGetSize, ICCompressGetSize macro [Windows Multimedia], _win32_ICCompressGetSize, multimedia.iccompressgetsize, vfw/ICCompressGetSize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	ICCompressGetSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICCompressGetSize macro


## -description



The <b>ICCompressGetSize</b> macro requests that the video compression driver supply the maximum size of one frame of data when compressed into the specified output format. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/6910e588-e60f-43b1-8fa6-113c2ec32a53">ICM_COMPRESS_GET_SIZE</a> message.




## -parameters




### -param hic

Handle to a compressor. 


### -param lpbiInput

Pointer to a BITMAPINFO structure containing the input format. 


### -param lpbiOutput

Pointer to a BITMAPINFO structure containing the output format. 


## -remarks



Typically, applications send this message to determine how large a buffer to allocate for the compressed frame.

The driver should calculate the size of the largest possible frame based on the input and output formats.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

