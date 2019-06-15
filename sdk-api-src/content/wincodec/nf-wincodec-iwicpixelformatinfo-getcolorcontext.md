---
UID: NF:wincodec.IWICPixelFormatInfo.GetColorContext
title: IWICPixelFormatInfo::GetColorContext (wincodec.h)
author: windows-sdk-content
description: Gets the pixel format's IWICColorContext.
old-location: wic\_wic_codec_iwicpixelformatinfo_getcolorcontext.htm
tech.root: wic
ms.assetid: c35fc474-cbf5-4705-b0f1-a2e24a062a7a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetColorContext, GetColorContext method [Windows Imaging Component], GetColorContext method [Windows Imaging Component],IWICPixelFormatInfo interface, IWICPixelFormatInfo interface [Windows Imaging Component],GetColorContext method, IWICPixelFormatInfo.GetColorContext, IWICPixelFormatInfo::GetColorContext, _wic_codec_iwicpixelformatinfo_getcolorcontext, wic._wic_codec_iwicpixelformatinfo_getcolorcontext, wincodec/IWICPixelFormatInfo::GetColorContext
ms.topic: method
f1_keywords: ["wincodec/IWICPixelFormatInfo.GetColorContext"]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICPixelFormatInfo.GetColorContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICPixelFormatInfo::GetColorContext


## -description


Gets the pixel format's <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>.


## -parameters




### -param ppIColorContext [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>**</b>

Pointer that receives the pixel format's color context.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The returned color context is the default color space for the pixel format. However, if an <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-imp-iwicbitmapsource">IWICBitmapSource</a> specifies its own color context, the source's context should be preferred over the pixel format's default.




