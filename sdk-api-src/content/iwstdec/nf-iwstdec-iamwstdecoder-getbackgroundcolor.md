---
UID: NF:iwstdec.IAMWstDecoder.GetBackgroundColor
title: IAMWstDecoder::GetBackgroundColor (iwstdec.h)
author: windows-sdk-content
description: Downstream filters use the GetBackgroundColor method to retrieve the current physical color used in color keying the background for overlay mixing.
old-location: dshow\iamwstdecoder_getbackgroundcolor.htm
tech.root: DirectShow
ms.assetid: 1661f2cd-8e6c-4e55-b5fd-995ef2962cb7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBackgroundColor, GetBackgroundColor method [DirectShow], GetBackgroundColor method [DirectShow],IAMWstDecoder interface, IAMWstDecoder interface [DirectShow],GetBackgroundColor method, IAMWstDecoder.GetBackgroundColor, IAMWstDecoder::GetBackgroundColor, IAMWstDecoderGetBackgroundColor, dshow.iamwstdecoder_getbackgroundcolor, iwstdec/IAMWstDecoder::GetBackgroundColor
ms.topic: method
f1_keywords: ["iwstdec/IAMWstDecoder.GetBackgroundColor"]
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
 - IAMWstDecoder.GetBackgroundColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMWstDecoder::GetBackgroundColor


## -description



Downstream filters use the <code>GetBackgroundColor</code> method to retrieve the current physical color used in color keying the background for overlay mixing.




## -parameters




### -param pdwPhysColor [out]

Receives the physical color as an RGB value.


## -returns



When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>
 

 

