---
UID: NN:wincodec.IWICBitmapFrameDecode
title: IWICBitmapFrameDecode (wincodec.h)
description: Defines methods for decoding individual image frames of an encoded file.
helpviewer_keywords: ["IWICBitmapFrameDecode","IWICBitmapFrameDecode interface [Windows Imaging Component]","IWICBitmapFrameDecode interface [Windows Imaging Component]","described","_wic_codec_iwicbitmapframedecode","wic._wic_codec_iwicbitmapframedecode","wincodec/IWICBitmapFrameDecode"]
old-location: wic\_wic_codec_iwicbitmapframedecode.htm
tech.root: wic
ms.assetid: 1498b800-6449-440f-bed7-85891637e559
ms.date: 12/05/2018
ms.keywords: IWICBitmapFrameDecode, IWICBitmapFrameDecode interface [Windows Imaging Component], IWICBitmapFrameDecode interface [Windows Imaging Component],described, _wic_codec_iwicbitmapframedecode, wic._wic_codec_iwicbitmapframedecode, wincodec/IWICBitmapFrameDecode
f1_keywords:
- wincodec/IWICBitmapFrameDecode
dev_langs:
- c++
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
- IWICBitmapFrameDecode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICBitmapFrameDecode interface


## -description


Defines methods for decoding individual image frames of an encoded file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapFrameDecode</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>. <b>IWICBitmapFrameDecode</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapFrameDecode</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts">GetColorContexts</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> associated with the image frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader">GetMetadataQueryReader</a>
</td>
<td align="left" width="63%">
Retrieves a metadata query reader for the frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail">GetThumbnail</a>
</td>
<td align="left" width="63%">
Retrieves a small preview of the frame, if supported by the codec.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85)">AITCodec Sample CODEC</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>



<b>Other Resources</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-guids-clsids">WIC GUIDs and CLSIDs</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-about-windows-imaging-codec">Windows Imaging Component Overview</a>
 

 

