---
UID: NF:wincodec.IWICBitmapFrameEncode.SetColorContexts
title: IWICBitmapFrameEncode::SetColorContexts (wincodec.h)
description: Sets a given number IWICColorContext profiles to the frame.
helpviewer_keywords: ["IWICBitmapFrameEncode interface [Windows Imaging Component]","SetColorContexts method","IWICBitmapFrameEncode.SetColorContexts","IWICBitmapFrameEncode::SetColorContexts","SetColorContexts","SetColorContexts method [Windows Imaging Component]","SetColorContexts method [Windows Imaging Component]","IWICBitmapFrameEncode interface","_wic_codec_iwicbitmapframeencode_setcolorcontexts","wic._wic_codec_iwicbitmapframeencode_setcolorcontexts","wincodec/IWICBitmapFrameEncode::SetColorContexts"]
old-location: wic\_wic_codec_iwicbitmapframeencode_setcolorcontexts.htm
tech.root: wic
ms.assetid: c955dede-297f-44c1-aa03-31a07a6d69d2
ms.date: 12/05/2018
ms.keywords: IWICBitmapFrameEncode interface [Windows Imaging Component],SetColorContexts method, IWICBitmapFrameEncode.SetColorContexts, IWICBitmapFrameEncode::SetColorContexts, SetColorContexts, SetColorContexts method [Windows Imaging Component], SetColorContexts method [Windows Imaging Component],IWICBitmapFrameEncode interface, _wic_codec_iwicbitmapframeencode_setcolorcontexts, wic._wic_codec_iwicbitmapframeencode_setcolorcontexts, wincodec/IWICBitmapFrameEncode::SetColorContexts
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICBitmapFrameEncode::SetColorContexts
 - wincodec/IWICBitmapFrameEncode::SetColorContexts
dev_langs:
 - c++
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
---

# IWICBitmapFrameEncode::SetColorContexts


## -description

Sets a given number <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> profiles to the frame.

## -parameters

### -param cCount [in]

Type: <b>UINT</b>

The number of <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> profiles to set.

### -param ppIColorContext [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>**</b>

A pointer to an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> pointer containing the color contexts profiles to set to the frame.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<ul>
<li><b>BMP</b>Setting color contexts is unsupported. This function will return <b>WINCODEC_ERR_UNSUPPORTEDOPERATION</b>.

</li>
<li><b>PNG</b>Setting at most one color context is supported, and additional color contexts will be ignored. This context must be a <a href="/windows/desktop/api/wincodec/ne-wincodec-wiccolorcontexttype">WICColorContextProfile</a>, and is used to encode the iCCP, gAMA, and cHRM chunks in the PNG file.

</li>
<li><b>JPEG, TIFF, JPEG-XR</b>Setting up to one <a href="/windows/desktop/api/wincodec/ne-wincodec-wiccolorcontexttype">WICColorContextProfile</a> and one  <a href="/windows/desktop/api/wincodec/ne-wincodec-wiccolorcontexttype">WICColorContextExifColorSpace</a> is supported. Users must not provide more than one of each type of color context, as all but the last context of each type will be ignored. In JPEG, the <b>WICColorContextProfile</b> is encoded to JPEG APP2 ICC metadata block.

In TIFF and JPEG-XR, the  <a href="/windows/desktop/api/wincodec/ne-wincodec-wiccolorcontexttype">WICColorContextProfile</a> is encoded to the IFD ICC profile metadata block (IFD tag 0x8773). In all three formats, the <a href="/windows/desktop/api/wincodec/ne-wincodec-wiccolorcontexttype">WICColorContextExifColorSpace</a> is encoded to EXIF colorspace metadata block (EXIF tag 0xA001).


</li>
</ul>