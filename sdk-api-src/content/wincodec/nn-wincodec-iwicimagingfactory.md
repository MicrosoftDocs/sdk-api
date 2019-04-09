---
UID: NN:wincodec.IWICImagingFactory
title: IWICImagingFactory (wincodec.h)
author: windows-sdk-content
description: Exposes methods used to create components for the Windows Imaging Component (WIC) such as decoders, encoders and pixel format converters.
old-location: wic\_wic_codec_iwicimagingfactory.htm
tech.root: wic
ms.assetid: 30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICImagingFactory, IWICImagingFactory interface [Windows Imaging Component], IWICImagingFactory interface [Windows Imaging Component],described, _wic_codec_iwicimagingfactory, wic._wic_codec_iwicimagingfactory, wincodec/IWICImagingFactory
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
 - IWICImagingFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICImagingFactory interface


## -description


Exposes methods used to create components for the Windows Imaging Component (WIC) such as decoders, encoders and pixel format converters.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICImagingFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICImagingFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICImagingFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76741d1e-3e1b-4018-b092-b668ecfd43c9">CreateBitmap</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0764fee2-0767-41a4-a681-b831abb04119">CreateBitmapClipper</a>
</td>
<td align="left" width="63%">
Creates a new instance of an <a href="https://msdn.microsoft.com/a21fb11f-8622-46d6-8612-875ac59d3fbf">IWICBitmapClipper</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec044a38-b39d-4421-8e56-a8be0586cc49">CreateBitmapFlipRotator</a>
</td>
<td align="left" width="63%">
Creates a new instance of an <a href="https://msdn.microsoft.com/1fcb19ba-34bd-48c0-9964-0c973c31cacc">IWICBitmapFlipRotator</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8483f352-c31b-4afe-a011-ebef3430c576">CreateBitmapFromHBITMAP</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a> from a bitmap handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a67695a1-30ac-4e28-a9a9-582601139e17">CreateBitmapFromHICON</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a> from an icon handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0fa8f55-2752-4494-8aac-6c47e0ba6e26">CreateBitmapFromMemory</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a> from a memory block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3b9057f-e39a-4e7b-a3dc-0942d55c25e0">CreateBitmapFromSource</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a> from a <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54111643-523a-4197-b7e9-ee0efeae5b88">CreateBitmapFromSourceRect</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a> from a specified rectangle of an <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4da6b185-4a94-4032-a1d6-e64b96a5da97">CreateBitmapScaler</a>
</td>
<td align="left" width="63%">
Creates a new instance of an <a href="https://msdn.microsoft.com/cc14be9d-d750-40db-a95f-309b392cefe8">IWICBitmapScaler</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60ae0ec4-2bf4-43f0-9882-ff8b6f5f5923">CreateColorContext</a>
</td>
<td align="left" width="63%">
Creates a new instance of the <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1cbe7987-2845-4d12-92f4-fcdd4ae6f370">CreateColorTransformer</a>
</td>
<td align="left" width="63%">
Creates a new instance of the <a href="https://msdn.microsoft.com/6c8ae787-3175-4128-ae9f-e11cb0e4c317">IWICColorTransform</a> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/810bf0c2-2780-4ba3-84c1-7b257139e26e">CreateComponentEnumerator</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/en-us/library/ms683764(v=VS.85).aspx">IEnumUnknown</a> object of the specified component types.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4feebf7-500f-4ab8-85fa-689edfe31846">CreateComponentInfo</a>
</td>
<td align="left" width="63%">
Creates a new instance of the <a href="https://msdn.microsoft.com/a31267ed-60cd-4de9-9fed-26bb390b29e6">IWICComponentInfo</a> class for the given component CLSID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d0072ce-3480-4687-a4ea-640953cf5a36">CreateDecoder</a>
</td>
<td align="left" width="63%">
Creates a new instance of the <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94cf408c-bcea-419a-bf87-fac1e15e0a12">CreateDecoderFromFileHandle</a>
</td>
<td align="left" width="63%">
Creates a new instance of the <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a> based on the given file handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/100c54c7-bb10-47dd-8436-04282ec6b110">CreateDecoderFromFilename</a>
</td>
<td align="left" width="63%">
Creates a new instance of the <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a> class based on the given file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9328715-54a0-4c9a-9977-3252068b7e4b">CreateDecoderFromStream</a>
</td>
<td align="left" width="63%">
Creates a new instance of the <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a> class based on the given <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7aae3ea6-2d8b-4764-9c78-a6cce49012a5">CreateEncoder</a>
</td>
<td align="left" width="63%">
Creates a new instance of the <a href="https://msdn.microsoft.com/fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad">IWICBitmapEncoder</a> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3264a987-4308-4c50-b99c-70142bc49476">CreateFastMetadataEncoderFromDecoder</a>
</td>
<td align="left" width="63%">
Creates a new instance of the fast metadata encoder based on the given <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/076cfd22-f744-4152-a1c0-1e0f17ac764d">CreateFastMetadataEncoderFromFrameDecode</a>
</td>
<td align="left" width="63%">
Creates a new instance of the fast metadata encoder based on the given image frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50ceabdf-574e-4083-86a4-dddd4da06bbf">CreateFormatConverter</a>
</td>
<td align="left" width="63%">
Creates a new instance of the <a href="https://msdn.microsoft.com/d558aaa7-5962-424c-9e83-363fba09ad50">IWICFormatConverter</a> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/135440ee-ea70-40da-9ee1-618a8e10170a">CreatePalette</a>
</td>
<td align="left" width="63%">
Creates a new instance of the <a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2998d22-68c5-45de-a651-6f67c6f5234a">CreateQueryWriter</a>
</td>
<td align="left" width="63%">
Creates a new instance of a query writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71c278f8-546f-4351-9e2c-b9cd9806ccfc">CreateQueryWriterFromReader</a>
</td>
<td align="left" width="63%">
Creates a new instance of a query writer based on the given query reader. The query writer will be pre-populated with metadata from the query reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c2ecaf0-5222-4f9b-96fb-5d2da72d11d4">CreateStream</a>
</td>
<td align="left" width="63%">
Creates a new instance of the <a href="https://msdn.microsoft.com/bc398732-037d-4f48-940f-c70975447972">IWICStream</a> class.

</td>
</tr>
</table> 

