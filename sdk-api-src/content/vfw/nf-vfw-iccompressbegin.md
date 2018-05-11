---
UID: NF:vfw.ICCompressBegin
title: ICCompressBegin macro
author: windows-driver-content
description: The ICCompressBegin macro notifies a video compression driver to prepare to compress data. You can use this macro or explicitly call the ICM_COMPRESS_BEGIN message.
old-location: multimedia\iccompressbegin.htm
old-project: Multimedia
ms.assetid: e09d3ac8-ead3-459c-a773-ffbe8198b40f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ICCompressBegin, ICCompressBegin macro [Windows Multimedia], _win32_ICCompressBegin, multimedia.iccompressbegin, vfw/ICCompressBegin
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	ICCompressBegin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICCompressBegin macro


## -description


The ICCompressBegin macro notifies a video compression driver to prepare to compress data. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/dd1d3a66-c625-4f55-b65a-8545c1c16301">ICM_COMPRESS_BEGIN</a> message.


## -parameters




### -param hic

Handle to a compressor.


### -param lpbiInput

Pointer to a <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFO</a> structure containing the input format.


### -param lpbiOutput

Pointer to a <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFO</a> structure containing the output format.


## -remarks



The driver should allocate and initialize any tables or memory that it needs for compressing the data formats when it receives the <a href="https://msdn.microsoft.com/d95b943f-458d-4a5e-bab1-e3648d323395">ICM_COMPRESS</a> message.

VCM saves the settings of the most recent <b>ICCompressBegin</b> macro. The <b>ICCompressBegin</b> and <b>ICCompressEnd</b> messages do not nest. If your driver receives <b>ICM_COMPRESS_BEGIN</b> before compression is stopped with <b>ICM_COMPRESS_END</b>, it should restart compression with new parameters.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

