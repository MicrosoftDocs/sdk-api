---
UID: NE:wincodec.WICBitmapDecoderCapabilities
title: WICBitmapDecoderCapabilities
author: windows-sdk-content
description: Specifies the capabilities of the decoder.
old-location: wic\_wic_codec_wicbitmapdecodercapabilities.htm
tech.root: wic
ms.assetid: e501b8f7-3c99-461d-be92-dca80f5657c5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: WICBitmapDecoderCapabilities, WICBitmapDecoderCapabilities enumeration [Windows Imaging Component], WICBitmapDecoderCapabilityCanDecodeAllImages, WICBitmapDecoderCapabilityCanDecodeSomeImages, WICBitmapDecoderCapabilityCanDecodeThumbnail, WICBitmapDecoderCapabilityCanEnumerateMetadata, WICBitmapDecoderCapabilitySameEncoder, _wic_codec_wicbitmapdecodercapabilities, wic._wic_codec_wicbitmapdecodercapabilities, wincodec/WICBitmapDecoderCapabilities, wincodec/WICBitmapDecoderCapabilityCanDecodeAllImages, wincodec/WICBitmapDecoderCapabilityCanDecodeSomeImages, wincodec/WICBitmapDecoderCapabilityCanDecodeThumbnail, wincodec/WICBitmapDecoderCapabilityCanEnumerateMetadata, wincodec/WICBitmapDecoderCapabilitySameEncoder
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICBitmapDecoderCapabilities
product: Windows
targetos: Windows
req.typenames: WICBitmapDecoderCapabilities
req.redist: 
---

# WICBitmapDecoderCapabilities enumeration


## -description


Specifies the capabilities of the decoder.


## -enum-fields




### -field WICBitmapDecoderCapabilitySameEncoder

Decoder recognizes the image was encoded with an encoder produced by the same vendor.
         




### -field WICBitmapDecoderCapabilityCanDecodeAllImages

Decoder can decode all the images within an image container.


### -field WICBitmapDecoderCapabilityCanDecodeSomeImages

Decoder can decode some of the images within an image container.


### -field WICBitmapDecoderCapabilityCanEnumerateMetadata

Decoder can enumerate the metadata blocks within a container format.


### -field WICBitmapDecoderCapabilityCanDecodeThumbnail

Decoder can find and decode a thumbnail.


### -field WICBITMAPDECODERCAPABILITIES_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a>
 

 

