---
UID: NF:iwstdec.IAMWstDecoder.SetBackgroundColor
title: IAMWstDecoder::SetBackgroundColor
author: windows-sdk-content
description: Downstream filters use the SetBackgroundColor method to assign the physical color to be used in color keying the background for overlay mixing.
old-location: dshow\iamwstdecoder_setbackgroundcolor.htm
old-project: DirectShow
ms.assetid: d65726aa-a826-41d4-95f3-40c86d7b9347
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IAMWstDecoder interface [DirectShow],SetBackgroundColor method, IAMWstDecoder.SetBackgroundColor, IAMWstDecoder::SetBackgroundColor, IAMWstDecoderSetBackgroundColor, SetBackgroundColor, SetBackgroundColor method [DirectShow], SetBackgroundColor method [DirectShow],IAMWstDecoder interface, dshow.iamwstdecoder_setbackgroundcolor, iwstdec/IAMWstDecoder::SetBackgroundColor
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AM_WST_STYLE, *PAM_WST_STYLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMWstDecoder.SetBackgroundColor
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAMWstDecoder::SetBackgroundColor


## -description



Downstream filters use the <code>SetBackgroundColor</code> method to assign the physical color to be used in color keying the background for overlay mixing.




## -parameters




### -param dwPhysColor [in]

Specifies a <b>DWORD</b> containing the physical color.


## -returns



When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/f2f5a459-14de-4be1-909c-3c23e4cfd737">IAMWstDecoder Interface</a>
 

 

