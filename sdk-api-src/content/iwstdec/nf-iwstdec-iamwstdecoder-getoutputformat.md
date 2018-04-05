---
UID: NF:iwstdec.IAMWstDecoder.GetOutputFormat
title: IAMWstDecoder::GetOutputFormat method
author: windows-driver-content
description: Downstream filters use the GetOutputFormat method to retrieve the size, bit depth, and other parameters of the output video.
old-location: dshow\iamwstdecoder_getoutputformat.htm
old-project: DirectShow
ms.assetid: 63ef7dbe-138b-442a-bf54-1f409c969418
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetOutputFormat method [DirectShow], GetOutputFormat method [DirectShow], IAMWstDecoder interface, GetOutputFormat,IAMWstDecoder.GetOutputFormat, IAMWstDecoder, IAMWstDecoder interface [DirectShow], GetOutputFormat method, IAMWstDecoder::GetOutputFormat, IAMWstDecoderGetOutputFormat, dshow.iamwstdecoder_getoutputformat, iwstdec/IAMWstDecoder::GetOutputFormat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: iwstdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AM_WST_STYLE, *PAM_WST_STYLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMWstDecoder.GetOutputFormat
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAMWstDecoder::GetOutputFormat method


## -description



Downstream filters use the <code>GetOutputFormat</code> method to retrieve the size, bit depth, and other parameters of the output video.




## -parameters




### -param lpbmih [out]

A pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure that receives the size, bit depth, and other properties of the output video.


## -returns



When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/f2f5a459-14de-4be1-909c-3c23e4cfd737">IAMWstDecoder Interface</a>
 

 

