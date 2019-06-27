---
UID: NN:wincodec.IWICFastMetadataEncoder
title: IWICFastMetadataEncoder (wincodec.h)
author: windows-sdk-content
description: Exposes methods used for in-place metadata editing. A fast metadata encoder enables you to add and remove metadata to an image without having to fully re-encode the image.
old-location: wic\_wic_codec_iwicfastmetadataencoder.htm
tech.root: wic
ms.assetid: c7b57a71-f1fe-4e30-a52e-72ab6ce021f7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICFastMetadataEncoder, IWICFastMetadataEncoder interface [Windows Imaging Component], IWICFastMetadataEncoder interface [Windows Imaging Component],described, _wic_codec_iwicfastmetadataencoder, wic._wic_codec_iwicfastmetadataencoder, wincodec/IWICFastMetadataEncoder
ms.topic: interface
f1_keywords: 
 - "wincodec/IWICFastMetadataEncoder"
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
 - IWICFastMetadataEncoder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICFastMetadataEncoder interface


## -description


Exposes methods used for in-place metadata editing. A fast metadata encoder enables you to add and remove metadata to an image without having to fully re-encode the image.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICFastMetadataEncoder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICFastMetadataEncoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICFastMetadataEncoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicfastmetadataencoder-commit">Commit</a>
</td>
<td align="left" width="63%">
Finalizes metadata changes to the image stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter">GetMetadataQueryWriter</a>
</td>
<td align="left" width="63%">
Retrieves a metadata query writer for fast metadata encoding.

</td>
</tr>
</table> 


## -remarks



A decoder must be created using the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wicdecodeoptions">WICDecodeOptions</a> value <b>WICDecodeMetadataCacheOnDemand</b> to perform in-place metadata updates. 
            Using the <b>WICDecodeMetadataCacheOnLoad</b> option causes the decoder to release the file stream necessary to perform the metadata updates. 
         

Not all metadata formats support fast metadata encoding. The native metadata handlers that support metadata are IFD, Exif, XMP, and GPS.
         

If a fast metadata encoder fails, the image will need to be fully re-encoded to add the metadata.
         


#### Examples

The following demonstrates how to obtain a fast metadata encoder from an image frame and use its query writer to write a metadata item.


```cpp
IWICFastMetadataEncoder *pFME = NULL;
IWICMetadataQueryWriter *pFMEQW = NULL;

hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(pFrameDecode, &pFME);

if (SUCCEEDED(hr))
{
 	hr = pFME->GetMetadataQueryWriter(&pFMEQW);
}

if (SUCCEEDED(hr))
{
	 // Add additional metadata
 	PROPVARIANT value;

	 PropVariantInit(&value);

 	value.vt = VT_UI2;
	 value.uiVal = 99;
 	hr = pFMEQW->SetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);

 	PropVariantClear(&value);
}

if (SUCCEEDED(hr))
{
	 hr = pFME->Commit();
}
```




