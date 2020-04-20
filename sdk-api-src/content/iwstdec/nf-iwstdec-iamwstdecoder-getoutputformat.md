---
UID: NF:iwstdec.IAMWstDecoder.GetOutputFormat
title: IAMWstDecoder::GetOutputFormat (iwstdec.h)
description: Downstream filters use the GetOutputFormat method to retrieve the size, bit depth, and other parameters of the output video.helpviewer_keywords: ["GetOutputFormat","GetOutputFormat method [DirectShow]","GetOutputFormat method [DirectShow]","IAMWstDecoder interface","IAMWstDecoder interface [DirectShow]","GetOutputFormat method","IAMWstDecoder.GetOutputFormat","IAMWstDecoder::GetOutputFormat","IAMWstDecoderGetOutputFormat","dshow.iamwstdecoder_getoutputformat","iwstdec/IAMWstDecoder::GetOutputFormat"]
old-location: dshow\iamwstdecoder_getoutputformat.htm
tech.root: DirectShow
ms.assetid: 63ef7dbe-138b-442a-bf54-1f409c969418
ms.date: 12/05/2018
ms.keywords: GetOutputFormat, GetOutputFormat method [DirectShow], GetOutputFormat method [DirectShow],IAMWstDecoder interface, IAMWstDecoder interface [DirectShow],GetOutputFormat method, IAMWstDecoder.GetOutputFormat, IAMWstDecoder::GetOutputFormat, IAMWstDecoderGetOutputFormat, dshow.iamwstdecoder_getoutputformat, iwstdec/IAMWstDecoder::GetOutputFormat
f1_keywords:
- iwstdec/IAMWstDecoder.GetOutputFormat
dev_langs:
- c++
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMWstDecoder.GetOutputFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMWstDecoder::GetOutputFormat


## -description



Downstream filters use the <code>GetOutputFormat</code> method to retrieve the size, bit depth, and other parameters of the output video.




## -parameters




### -param lpbmih [out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure that receives the size, bit depth, and other properties of the output video.


## -returns



When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>
 

 

