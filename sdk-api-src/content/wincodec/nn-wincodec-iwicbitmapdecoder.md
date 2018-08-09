---
UID: NN:wincodec.IWICBitmapDecoder
title: IWICBitmapDecoder
author: windows-sdk-content
description: Exposes methods that represent a decoder.
old-location: wic\_wic_codec_iwicbitmapdecoder.htm
old-project: wic
ms.assetid: 91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWICBitmapDecoder, IWICBitmapDecoder interface [Windows Imaging Component], IWICBitmapDecoder interface [Windows Imaging Component],described, _wic_codec_iwicbitmapdecoder, wic._wic_codec_iwicbitmapdecoder, wincodec/IWICBitmapDecoder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - Windowscodecs.dll
api_name:
 - IWICBitmapDecoder
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapDecoder interface


## -description


Exposes methods that represent a decoder.

The interface provides access to the decoder's properties such as global thumbnails (if supported), frames, and palette. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapDecoder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICBitmapDecoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapDecoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a387936-b045-42c7-b57c-1ac470640a14">CopyPalette</a>
</td>
<td align="left" width="63%">
Copies the decoder's <a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a> .

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55fdf9c0-5fa4-46e2-b4d2-42b8d4c90887">GetColorContexts</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a> objects of the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba7b64cf-28de-40d9-80f1-f4b5b1909b77">GetContainerFormat</a>
</td>
<td align="left" width="63%">
Retrieves the image's container format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45bcdcda-c45a-4646-a511-3a16d3fda262">GetDecoderInfo</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/7edc6d1a-7eda-45ef-bf1d-c5835b37a90f">IWICBitmapDecoderInfo</a> for the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e8c1cfd-50f3-431c-aedb-6e57d1368695">GetFrame</a>
</td>
<td align="left" width="63%">
Retrieves the specified frame of the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16eb613d-f649-436d-a121-e6468cd2581a">GetFrameCount</a>
</td>
<td align="left" width="63%">
Retrieves the total number of frames in the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/353ce6d8-ef33-44b6-ab8a-7c5903a024f6">GetMetadataQueryReader</a>
</td>
<td align="left" width="63%">
Retrieves the metadata query reader from the decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e726eba-bb74-45b8-be6b-63d9ce00c272">GetPreview</a>
</td>
<td align="left" width="63%">
Retrieves a preview image, if supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbfe61d9-50ca-4d44-a8a3-2acae3413985">GetThumbnail</a>
</td>
<td align="left" width="63%">
Retrieves a bitmap thumbnail of the image, if one exists

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the decoder with the provided stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eeff3d5d-ed7f-41f7-b529-aeeeb8503a50">QueryCapability</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the decoder based on the specified stream.

</td>
</tr>
</table> 


## -remarks



There are a number of concrete implemenations of this interface representing each of the standard decoders provided by the platform including bitmap (BMP), Portable Network Graphics (PNG), icon (ICO), Joint Photographic Experts Group (JPEG), Graphics Interchange Format (GIF), Tagged Image File Format (TIFF), and Microsoft Windows Digital Photo (WDP). The following table includes the class identifier (CLSID) for each native decoder.
            

<table class="clsStd">
<tr>
<th>CLSID Name</th>
<th>CLSID</th>
</tr>
<tr>
<td>CLSID_WICBmpDecoder</td>
<td>0x6b462062, 0x7cbf, 0x400d, 0x9f, 0xdb, 0x81, 0x3d, 0xd1, 0xf, 0x27, 0x78</td>
</tr>
<tr>
<td>CLSID_WICPngDecoder</td>
<td>0x389ea17b, 0x5078, 0x4cde, 0xb6, 0xef, 0x25, 0xc1, 0x51, 0x75, 0xc7, 0x51</td>
</tr>
<tr>
<td>CLSID_WICIcoDecoder</td>
<td>0xc61bfcdf, 0x2e0f, 0x4aad, 0xa8, 0xd7, 0xe0, 0x6b, 0xaf, 0xeb, 0xcd, 0xfe</td>
</tr>
<tr>
<td>CLSID_WICJpegDecoder</td>
<td>0x9456a480, 0xe88b, 0x43ea, 0x9e, 0x73, 0xb, 0x2d, 0x9b, 0x71, 0xb1, 0xca</td>
</tr>
<tr>
<td>CLSID_WICGifDecoder</td>
<td>0x381dda3c, 0x9ce9, 0x4834, 0xa2, 0x3e, 0x1f, 0x98, 0xf8, 0xfc, 0x52, 0xbe</td>
</tr>
<tr>
<td>CLSID_WICTiffDecoder</td>
<td>0xb54e85d9, 0xfe23, 0x499f, 0x8b, 0x88, 0x6a, 0xce, 0xa7, 0x13, 0x75, 0x2b</td>
</tr>
<tr>
<td>CLSID_WICWmpDecoder</td>
<td>0xa26cec36, 0x234c, 0x4950, 0xae, 0x16, 0xe3, 0x4a, 0xac, 0xe7, 0x1d, 0x0d</td>
</tr>
</table>
 

This interface may be sub-classed to provide support for third party codecs as part of the extensibility model. See the <a href="http://msdn.microsoft.com/en-us/library/ms771770.aspx">AITCodec Sample CODEC</a>.

Codecs written as TIFF container formats that are not register will decode as a TIFF image. Client applications should check for a zero frame count to determine if the codec is valid.




## -see-also




<a href="f6a44610-0d30-420e-aaf9-c7f436f3c195">AITCodec Sample CODEC</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/58f03dc2-cc31-4d76-b75a-f332da1f900f">How to Write a WIC-Enabled CODEC</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/2be5cfeb-2dd3-4486-b639-35ee28a7dd7b">WIC GUIDs and CLSIDs</a>



<a href="https://msdn.microsoft.com/a05b496a-bd4c-4065-8060-df0f8930cde7">Windows Imaging Component Overview</a>
 

 

