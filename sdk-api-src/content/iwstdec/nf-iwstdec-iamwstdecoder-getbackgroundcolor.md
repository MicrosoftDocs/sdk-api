---
UID: NF:iwstdec.IAMWstDecoder.GetBackgroundColor
title: IAMWstDecoder::GetBackgroundColor
author: windows-driver-content
description: Downstream filters use the GetBackgroundColor method to retrieve the current physical color used in color keying the background for overlay mixing.
old-location: dshow\iamwstdecoder_getbackgroundcolor.htm
old-project: DirectShow
ms.assetid: 1661f2cd-8e6c-4e55-b5fd-995ef2962cb7
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: GetBackgroundColor, GetBackgroundColor method [DirectShow], GetBackgroundColor method [DirectShow],IAMWstDecoder interface, IAMWstDecoder interface [DirectShow],GetBackgroundColor method, IAMWstDecoder.GetBackgroundColor, IAMWstDecoder::GetBackgroundColor, IAMWstDecoderGetBackgroundColor, dshow.iamwstdecoder_getbackgroundcolor, iwstdec/IAMWstDecoder::GetBackgroundColor
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
-	IAMWstDecoder.GetBackgroundColor
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/f2f5a459-14de-4be1-909c-3c23e4cfd737">IAMWstDecoder Interface</a>
 

 

