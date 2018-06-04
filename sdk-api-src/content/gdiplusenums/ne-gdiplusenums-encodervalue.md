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

# EncoderValue enumeration


## -description


The <b>EncoderValue</b> enumeration specifies values that can be passed as arguments to image encoders. For more information about image encoders, see <a href="https://msdn.microsoft.com/f9a5b4b1-4e25-42c8-a96b-a3104841e5f3">Using Image Encoders and Decoders</a> .


## -enum-fields




### -field EncoderValueColorTypeCMYK

Not used in GDI+ version 1.0. 


### -field EncoderValueColorTypeYCCK

Not used in GDI+ version 1.0. 


### -field EncoderValueCompressionLZW

For a TIFF image, specifies the LZW compression method. 


### -field EncoderValueCompressionCCITT3

For a TIFF image, specifies the CCITT3 compression method. 


### -field EncoderValueCompressionCCITT4

For a TIFF image, specifies the CCITT4 compression method. 


### -field EncoderValueCompressionRle

For a TIFF image, specifies the RLE compression method. 


### -field EncoderValueCompressionNone

For a TIFF image, specifies no compression. 


### -field EncoderValueScanMethodInterlaced

Not used in GDI+ version 1.0. 


### -field EncoderValueScanMethodNonInterlaced

Not used in GDI+ version 1.0. 


### -field EncoderValueVersionGif87

Not used in GDI+ version 1.0. 


### -field EncoderValueVersionGif89

Not used in GDI+ version 1.0. 


### -field EncoderValueRenderProgressive

Not used in GDI+ version 1.0. 


### -field EncoderValueRenderNonProgressive

Not used in GDI+ version 1.0. 


### -field EncoderValueTransformRotate90

For a JPEG image, specifies lossless 90-degree clockwise rotation. 


### -field EncoderValueTransformRotate180

For a JPEG image, specifies lossless 180-degree rotation. 


### -field EncoderValueTransformRotate270

For a JPEG image, specifies lossless 270-degree clockwise rotation. 


### -field EncoderValueTransformFlipHorizontal

For a JPEG image, specifies a lossless horizontal flip. 


### -field EncoderValueTransformFlipVertical

For a JPEG image, specifies a lossless vertical flip. 


### -field EncoderValueMultiFrame

Specifies multiple-frame encoding. 


### -field EncoderValueLastFrame

Specifies the last frame of a multiple-frame image. 


### -field EncoderValueFlush

Specifies that the encoder object is to be closed. 


### -field EncoderValueFrameDimensionTime

Not used in GDI+ version 1.0. 


### -field EncoderValueFrameDimensionResolution

Not used in GDI+ version 1.0. 


### -field EncoderValueFrameDimensionPage

For a TIFF image, specifies the page frame dimension 


### -field EncoderValueColorTypeGray


### -field EncoderValueColorTypeRGB



