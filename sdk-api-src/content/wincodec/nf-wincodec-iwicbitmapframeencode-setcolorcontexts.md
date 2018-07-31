---
UID: NF:wincodec.IWICBitmapFrameEncode.SetColorContexts
title: IWICBitmapFrameEncode::SetColorContexts
author: windows-sdk-content
description: Sets a given number IWICColorContext profiles to the frame.
old-location: wic\_wic_codec_iwicbitmapframeencode_setcolorcontexts.htm
old-project: wic
ms.assetid: c955dede-297f-44c1-aa03-31a07a6d69d2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWICBitmapFrameEncode interface [Windows Imaging Component],SetColorContexts method, IWICBitmapFrameEncode.SetColorContexts, IWICBitmapFrameEncode::SetColorContexts, SetColorContexts, SetColorContexts method [Windows Imaging Component], SetColorContexts method [Windows Imaging Component],IWICBitmapFrameEncode interface, _wic_codec_iwicbitmapframeencode_setcolorcontexts, wic._wic_codec_iwicbitmapframeencode_setcolorcontexts, wincodec/IWICBitmapFrameEncode::SetColorContexts
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICBitmapFrameEncode.SetColorContexts
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapFrameEncode::SetColorContexts


## -description


Sets a given number <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a> profiles to the frame.


## -parameters




### -param cCount [in]

Type: <b>UINT</b>

The number of <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a> profiles to set.


### -param ppIColorContext [in]

Type: <b><a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a>**</b>

A pointer to an <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a> pointer containing the color contexts profiles to set to the frame.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<ul>
<li><b>BMP</b>Setting color contexts is unsupported. This function will return <b>WINCODEC_ERR_UNSUPPORTEDOPERATION</b>.

</li>
<li><b>PNG</b>Setting at most one color context is supported, and additional color contexts will be ignored. This context must be a <a href="_wic_codec_wiccolorcontexttype.htm">WICColorContextProfile</a>, and is used to encode the iCCP, gAMA, and cHRM chunks in the PNG file.

</li>
<li><b>JPEG, TIFF, JPEG-XR</b>Setting up to one <a href="_wic_codec_wiccolorcontexttype.htm">WICColorContextProfile</a> and one  <a href="_wic_codec_wiccolorcontexttype.htm">WICColorContextExifColorSpace</a> is supported. Users must not provide more than one of each type of color context, as all but the last context of each type will be ignored. In JPEG, the <b>WICColorContextProfile</b> is encoded to JPEG APP2 ICC metadata block.

In TIFF and JPEG-XR, the  <a href="_wic_codec_wiccolorcontexttype.htm">WICColorContextProfile</a> is encoded to the IFD ICC profile metadata block (IFD tag 0x8773). In all three formats, the <a href="_wic_codec_wiccolorcontexttype.htm">WICColorContextExifColorSpace</a> is encoded to EXIF colorspace metadata block (EXIF tag 0xA001).


</li>
</ul>


