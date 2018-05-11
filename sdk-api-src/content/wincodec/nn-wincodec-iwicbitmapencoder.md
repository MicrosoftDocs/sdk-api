---
UID: NN:wincodec.IWICBitmapEncoder
title: IWICBitmapEncoder
author: windows-driver-content
description: Defines methods for setting an encoder's properties such as thumbnails, frames, and palettes.
old-location: wic\_wic_codec_iwicbitmapencoder.htm
old-project: wic
ms.assetid: fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWICBitmapEncoder, IWICBitmapEncoder interface [Windows Imaging Component], IWICBitmapEncoder interface [Windows Imaging Component],described, _wic_codec_iwicbitmapencoder, wic._wic_codec_iwicbitmapencoder, wincodec/IWICBitmapEncoder
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
-	wincodec.h
api_name:
-	IWICBitmapEncoder
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapEncoder interface


## -description


Defines methods for setting an encoder's properties such as thumbnails, frames, and palettes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapEncoder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICBitmapEncoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapEncoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a>
</td>
<td align="left" width="63%">
Commits all changes for the image and closes the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c48f603-e7be-4b0c-a262-0dd01308e868">CreateNewFrame</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a> instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d197321-0a89-49fd-b243-1d870c178b57">GetContainerFormat</a>
</td>
<td align="left" width="63%">
Retrieves the encoder's container format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af723a68-89c8-4d0c-88ef-cda4abaad6f7">GetEncoderInfo</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/152b0dd2-1e5e-47fc-b6eb-a4c042e65047">IWICBitmapEncoderInfo</a> for the encoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11160c48-dbbe-45b6-864c-6a6713ec9ab5">GetMetadataQueryWriter</a>
</td>
<td align="left" width="63%">
Retrieves a metadata query writer for the encoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the encoder with an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> which tells the encoder where to encode the bits.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68e64db9-ee6a-4dc3-bf74-34274211e2dc">SetColorContexts</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a> objects for the encoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9310f407-d310-402b-bd90-ebc7e8d99361">SetPalette</a>
</td>
<td align="left" width="63%">
Sets the global palette for the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca02236d-9434-4db5-84af-9331f23e20a7">SetPreview</a>
</td>
<td align="left" width="63%">
Sets the global preview for the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecabfde8-0079-4059-8691-bbe3f0baa934">SetThumbnail</a>
</td>
<td align="left" width="63%">
Sets the global thumbnail for the image.

</td>
</tr>
</table> 


## -remarks



There are a number of concrete implemenations of this interface representing each of the standard encoders provided by the platform including bitmap (BMP), Portable Network Graphics (PNG), Joint Photographic Experts Group (JPEG), Graphics Interchange Format (GIF), Tagged Image File Format (TIFF), and Microsoft Windows Digital Photo (WDP). The following table includes the class identifier (CLSID) for each native encoder.
            

<table class="clsStd">
<tr>
<th>CLSID Name</th>
<th>CLSID</th>
</tr>
<tr>
<td>CLSID_WICBmpEncoder</td>
<td>0x69be8bb4, 0xd66d, 0x47c8, 0x86, 0x5a, 0xed, 0x15, 0x89, 0x43, 0x37, 0x82</td>
</tr>
<tr>
<td>CLSID_WICPngEncoder</td>
<td>0x27949969, 0x876a, 0x41d7, 0x94, 0x47, 0x56, 0x8f, 0x6a, 0x35, 0xa4, 0xdc</td>
</tr>
<tr>
<td>CLSID_WICJpegEncoder</td>
<td>0x1a34f5c1, 0x4a5a, 0x46dc, 0xb6, 0x44, 0x1f, 0x45, 0x67, 0xe7, 0xa6, 0x76</td>
</tr>
<tr>
<td>CLSID_WICGifEncoder</td>
<td>0x114f5598, 0xb22, 0x40a0, 0x86, 0xa1, 0xc8, 0x3e, 0xa4, 0x95, 0xad, 0xbd</td>
</tr>
<tr>
<td>CLSID_WICTiffEncoder</td>
<td>0x0131be10, 0x2001, 0x4c5f, 0xa9, 0xb0, 0xcc, 0x88, 0xfa, 0xb6, 0x4c, 0xe8</td>
</tr>
<tr>
<td>CLSID_WICWmpEncoder</td>
<td>0xac4ce3cb, 0xe1c1, 0x44cd, 0x82, 0x15, 0x5a, 0x16, 0x65, 0x50, 0x9e, 0xc2</td>
</tr>
</table>
 

Additionally this interface may be sub-classed to provide support for third party codecs as part of the extensibility model. See the <a href="http://msdn.microsoft.com/en-us/library/ms771770.aspx">AITCodec Sample CODEC</a>.




## -see-also




<a href="http://msdn.microsoft.com/en-us/library/ms771770.aspx">AITCodec Sample CODEC</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/58f03dc2-cc31-4d76-b75a-f332da1f900f">How to Write a WIC-Enabled CODEC</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/2be5cfeb-2dd3-4486-b639-35ee28a7dd7b">WIC GUIDs and CLSIDs</a>



<a href="https://msdn.microsoft.com/a05b496a-bd4c-4065-8060-df0f8930cde7">Windows Imaging Component Overview</a>
 

 

