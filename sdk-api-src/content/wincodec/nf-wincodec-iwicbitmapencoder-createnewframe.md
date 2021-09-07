---
UID: NF:wincodec.IWICBitmapEncoder.CreateNewFrame
title: IWICBitmapEncoder::CreateNewFrame (wincodec.h)
description: Creates a new IWICBitmapFrameEncode instance.
helpviewer_keywords: ["CreateNewFrame","CreateNewFrame method [Windows Imaging Component]","CreateNewFrame method [Windows Imaging Component]","IWICBitmapEncoder interface","IWICBitmapEncoder interface [Windows Imaging Component]","CreateNewFrame method","IWICBitmapEncoder.CreateNewFrame","IWICBitmapEncoder::CreateNewFrame","_wic_codec_iwicbitmapencoder_createnewframe","wic._wic_codec_iwicbitmapencoder_createnewframe","wincodec/IWICBitmapEncoder::CreateNewFrame"]
old-location: wic\_wic_codec_iwicbitmapencoder_createnewframe.htm
tech.root: wic
ms.assetid: 1c48f603-e7be-4b0c-a262-0dd01308e868
ms.date: 12/05/2018
ms.keywords: CreateNewFrame, CreateNewFrame method [Windows Imaging Component], CreateNewFrame method [Windows Imaging Component],IWICBitmapEncoder interface, IWICBitmapEncoder interface [Windows Imaging Component],CreateNewFrame method, IWICBitmapEncoder.CreateNewFrame, IWICBitmapEncoder::CreateNewFrame, _wic_codec_iwicbitmapencoder_createnewframe, wic._wic_codec_iwicbitmapencoder_createnewframe, wincodec/IWICBitmapEncoder::CreateNewFrame
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICBitmapEncoder::CreateNewFrame
 - wincodec/IWICBitmapEncoder::CreateNewFrame
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapEncoder.CreateNewFrame
---

# IWICBitmapEncoder::CreateNewFrame


## -description

Creates a new <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncode</a> instance.

## -parameters

### -param ppIFrameEncode [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncode</a>**</b>

A pointer that receives a pointer to the new instance of an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncode</a>.

### -param ppIEncoderOptions [in, out]

Type: <b><a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)">IPropertyBag2</a>**</b>

Optional. Receives the named properties to use for subsequent frame initialization. See Remarks.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The parameter <i>ppIEncoderOptions</i> can be used to receive an <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)">IPropertyBag2</a> that can then be used to specify encoder options. This is done by passing a pointer to a <b>NULL</b> IPropertyBag2 pointer in <i>ppIEncoderOptions</i>. The returned IPropertyBag2 is initialized with all encoder options that are available for the given format, at their default values. To specify non-default encoding behavior, set the needed encoder options on the IPropertyBag2 and pass it to <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-initialize">IWICBitmapFrameEncode::Initialize</a>.

<div class="alert"><b>Note</b>  Do not pass in a pointer to an initialized <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)">IPropertyBag2</a>. The pointer will be overwritten, and the original IPropertyBag2 will not be freed.</div>
<div> </div>
Otherwise, you can pass <b>NULL</b> in <i>ppIEncoderOptions</i> if you do not intend to specify encoder options.

See <a href="/windows/desktop/wic/-wic-creating-encoder">Encoding Overview</a> for an example of how to set encoder options.

For formats that support encoding multiple frames (for example, TIFF, JPEG-XR), you can work on only one frame at a time. This means that you must call <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-commit">IWICBitmapFrameEncode::Commit</a> before you call <b>CreateNewFrame</b> again.

## -see-also

<a href="/windows/desktop/wic/-wic-creating-encoder">Encoding Overview</a>



<a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)">IPropertyBag2</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder">IWICBitmapEncoder</a>