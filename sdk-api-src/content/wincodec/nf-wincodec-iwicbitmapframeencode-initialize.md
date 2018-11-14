---
UID: NF:wincodec.IWICBitmapFrameEncode.Initialize
title: IWICBitmapFrameEncode::Initialize
author: windows-sdk-content
description: Initializes the frame encoder using the given properties.
old-location: wic\_wic_codec_iwicbitmapframeencode_initialize.htm
tech.root: wic
ms.assetid: ec215e32-b4bd-469a-903d-f5b546185183
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWICBitmapFrameEncode interface [Windows Imaging Component],Initialize method, IWICBitmapFrameEncode.Initialize, IWICBitmapFrameEncode::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICBitmapFrameEncode interface, _wic_codec_iwicbitmapframeencode_initialize, wic._wic_codec_iwicbitmapframeencode_initialize, wincodec/IWICBitmapFrameEncode::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapFrameEncode.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wincodec.h
: 
- IWICBitmapFrameEncode.Initialize
: 
---

# IWICBitmapFrameEncode::Initialize


## -description


Initializes the frame encoder using the given properties.


## -parameters




### -param pIEncoderOptions [in]

Type: <b><a href="https://msdn.microsoft.com/library/Aa768192(v=VS.85).aspx">IPropertyBag2</a>*</b>

The set of properties to use for <a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a> initialization.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If you don't want any encoding options, pass <b>NULL</b> for <i>pIEncoderOptions</i>. Otherwise, pass the <a href="https://msdn.microsoft.com/library/Aa768192(v=VS.85).aspx">IPropertyBag2</a> that was provided by <a href="https://msdn.microsoft.com/1c48f603-e7be-4b0c-a262-0dd01308e868">IWICBitmapEncoder::CreateNewFrame</a> with updated values.


For a complete list of encoding options supported by the Windows-provided codecs, see <a href="https://msdn.microsoft.com/8D3E4B3A-FA39-475C-B177-61FC81E5FFCC">Native WIC Codecs</a>. 



