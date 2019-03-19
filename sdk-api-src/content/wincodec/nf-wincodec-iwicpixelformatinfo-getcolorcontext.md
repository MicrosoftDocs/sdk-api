---
UID: NF:wincodec.IWICPixelFormatInfo.GetColorContext
title: IWICPixelFormatInfo::GetColorContext (wincodec.h)
author: windows-sdk-content
description: Gets the pixel format's IWICColorContext.
old-location: wic\_wic_codec_iwicpixelformatinfo_getcolorcontext.htm
tech.root: wic
ms.assetid: c35fc474-cbf5-4705-b0f1-a2e24a062a7a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetColorContext, GetColorContext method [Windows Imaging Component], GetColorContext method [Windows Imaging Component],IWICPixelFormatInfo interface, IWICPixelFormatInfo interface [Windows Imaging Component],GetColorContext method, IWICPixelFormatInfo.GetColorContext, IWICPixelFormatInfo::GetColorContext, _wic_codec_iwicpixelformatinfo_getcolorcontext, wic._wic_codec_iwicpixelformatinfo_getcolorcontext, wincodec/IWICPixelFormatInfo::GetColorContext
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
---

# IWICPixelFormatInfo::GetColorContext


## -description


Gets the pixel format's <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a>.


## -parameters




### -param ppIColorContext [out]

Type: <b><a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a>**</b>

Pointer that receives the pixel format's color context.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The returned color context is the default color space for the pixel format. However, if an <a href="https://msdn.microsoft.com/d092e9e5-c041-42f5-84c8-0af52bb5c810">IWICBitmapSource</a> specifies its own color context, the source's context should be preferred over the pixel format's default.




