---
UID: NF:iwstdec.IAMWstDecoder.GetDecoderLevel
title: IAMWstDecoder::GetDecoderLevel
author: windows-sdk-content
description: Applications use the GetDecoderLevel method to retrieve the WST decoder level. This method is not implemented and always returns AM_WST_LEVEL_1_5.
old-location: dshow\iamwstdecoder_getdecoderlevel.htm
tech.root: DirectShow
ms.assetid: 629ee71d-7d79-4fa9-b169-3b5328659435
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetDecoderLevel, GetDecoderLevel method [DirectShow], GetDecoderLevel method [DirectShow],IAMWstDecoder interface, IAMWstDecoder interface [DirectShow],GetDecoderLevel method, IAMWstDecoder.GetDecoderLevel, IAMWstDecoder::GetDecoderLevel, IAMWstDecoderGetDecoderLevel, dshow.iamwstdecoder_getdecoderlevel, iwstdec/IAMWstDecoder::GetDecoderLevel
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
 - IAMWstDecoder.GetDecoderLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMWstDecoder::GetDecoderLevel


## -description



Applications use the <code>GetDecoderLevel</code> method to retrieve the WST decoder level. This method is not implemented and always returns AM_WST_LEVEL_1_5.




## -parameters




### -param lpLevel [out]

Receives a member of the <a href="https://msdn.microsoft.com/e9186beb-5496-49c3-a76c-febb38b5b344">AM_WST_LEVEL</a> enumeration, indicting the decoder level.


## -returns



When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/f2f5a459-14de-4be1-909c-3c23e4cfd737">IAMWstDecoder Interface</a>
 

 

