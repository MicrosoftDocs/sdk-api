---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

