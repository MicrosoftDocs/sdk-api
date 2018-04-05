---
UID: NF:wincodec.IWICBitmapFrameEncode.SetResolution
title: IWICBitmapFrameEncode::SetResolution method
author: windows-driver-content
description: Sets the physical resolution of the output image.
old-location: wic\_wic_codec_iwicbitmapframeencode_setresolution.htm
old-project: wic
ms.assetid: 0b9e564a-5278-41d7-84ab-8b7594e776c7
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: IWICBitmapFrameEncode, IWICBitmapFrameEncode interface [Windows Imaging Component], SetResolution method, IWICBitmapFrameEncode::SetResolution, SetResolution method [Windows Imaging Component], SetResolution method [Windows Imaging Component], IWICBitmapFrameEncode interface, SetResolution,IWICBitmapFrameEncode.SetResolution, _wic_codec_iwicbitmapframeencode_setresolution, wic._wic_codec_iwicbitmapframeencode_setresolution, wincodec/IWICBitmapFrameEncode::SetResolution
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICBitmapFrameEncode.SetResolution
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapFrameEncode::SetResolution method


## -description


Sets the physical resolution of the output image.


## -parameters




### -param dpiX [in]

Type: <b>double</b>

The horizontal resolution value.


### -param dpiY [in]

Type: <b>double</b>

The vertical resolution value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Windows Imaging Component (WIC) doesn't perform any special processing as a result of DPI resolution values. For example, data returned from <a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">IWICBitmapSource::CopyPixels</a> isn't scaled by the DPI. The app must handle DPI resolution.




