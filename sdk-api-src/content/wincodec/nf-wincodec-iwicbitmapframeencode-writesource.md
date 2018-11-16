---
UID: NF:wincodec.IWICBitmapFrameEncode.WriteSource
title: IWICBitmapFrameEncode::WriteSource
author: windows-sdk-content
description: Encodes a bitmap source.
old-location: wic\_wic_codec_iwicbitmapframeencode_writesource.htm
tech.root: wic
ms.assetid: bc748982-6dc8-41cc-a23b-9d127dc22a1f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWICBitmapFrameEncode interface [Windows Imaging Component],WriteSource method, IWICBitmapFrameEncode.WriteSource, IWICBitmapFrameEncode::WriteSource, WriteSource, WriteSource method [Windows Imaging Component], WriteSource method [Windows Imaging Component],IWICBitmapFrameEncode interface, _wic_codec_iwicbitmapframeencode_writesource, wic._wic_codec_iwicbitmapframeencode_writesource, wincodec/IWICBitmapFrameEncode::WriteSource
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
 - IWICBitmapFrameEncode.WriteSource
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
- IWICBitmapFrameEncode.WriteSource
: 
---

# IWICBitmapFrameEncode::WriteSource


## -description


Encodes a bitmap source.


## -parameters




### -param pIBitmapSource [in]

Type: <b><a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>*</b>

The bitmap source to encode.


### -param prc [in]

Type: <b><a href="https://msdn.microsoft.com/e07c26bf-b645-4382-bb93-8472ba397026">WICRect</a>*</b>

The size rectangle of the bitmap source.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <a href="https://msdn.microsoft.com/e21e1a66-b1fa-4700-a14e-dc382b5404f7">SetSize</a> is not called prior to calling <b>WriteSource</b>, the size given in <i>prc</i> is used if not <b>NULL</b>. Otherwise, the size of the <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> given in <i>pIBitmapSource</i> is used. 

If <a href="https://msdn.microsoft.com/9327b5dd-18a3-40c6-8bb4-245fcc7fb582">SetPixelFormat</a> is not called prior to calling <b>WriteSource</b>, the pixel format of the <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> given in <i>pIBitmapSource</i> is used.

If <a href="https://msdn.microsoft.com/0b9e564a-5278-41d7-84ab-8b7594e776c7">SetResolution</a> is not called prior to calling <b>WriteSource</b>, the pixel format of <i>pIBitmapSource</i> is used.

If <a href="https://msdn.microsoft.com/c463fc95-695d-4ba3-bf62-5b09d69c60c2">SetPalette</a> is not called prior to calling <b>WriteSource</b>, the target pixel format is indexed, and the pixel format of <i>pIBitmapSource</i> matches the encoder frame's pixel format, then the <i>pIBitmapSource</i> pixel format is used.

When encoding a GIF image, if the global palette is set and the frame level palette is not set directly by the user or by a custom independent software vendor (ISV) GIF codec, <b>WriteSource</b> will use the global palette to encode the frame even when <i>pIBitmapSource</i> has a frame level palette.

Starting with  Windows Vista, repeated <b>WriteSource</b> calls can be made as long as the total accumulated source rect height is the same as set through <a href="https://msdn.microsoft.com/e21e1a66-b1fa-4700-a14e-dc382b5404f7">SetSize</a>.

Starting with Windows 8.1, the source rect must be at least the dimensions set through <a href="https://msdn.microsoft.com/e21e1a66-b1fa-4700-a14e-dc382b5404f7">SetSize</a>. If the source rect width exceeds the <b>SetSize</b> width, extra pixels on the right side are ignored. If the source rect height exceeds the remaining unfilled height, extra scan lines on the bottom are ignored.





## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/58f03dc2-cc31-4d76-b75a-f332da1f900f">How to Write a WIC-Enabled CODEC</a>



<a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a>



<a href="https://msdn.microsoft.com/a05b496a-bd4c-4065-8060-df0f8930cde7">Windows Imaging Component Overview</a>
 

 

