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

# WICTiffCompressionOption enumeration


## -description


Specifies the Tagged Image File Format (TIFF) compression options.


## -enum-fields




### -field WICTiffCompressionDontCare

Indicates a suitable compression algorithm based on the image and pixel format.


### -field WICTiffCompressionNone

Indicates no compression.


### -field WICTiffCompressionCCITT3

Indicates a CCITT3 compression algorithm. This algorithm is only valid for 1bpp pixel formats.


### -field WICTiffCompressionCCITT4

Indicates a CCITT4 compression algorithm. This algorithm is only valid for 1bpp pixel formats.


### -field WICTiffCompressionLZW

Indicates a LZW compression algorithm.


### -field WICTiffCompressionRLE

Indicates a RLE compression algorithm. This algorithm is only valid for 1bpp pixel formats.


### -field WICTiffCompressionZIP

Indicates a ZIP compression algorithm.


### -field WICTiffCompressionLZWHDifferencing

Indicates an LZWH differencing algorithm.


### -field WICTIFFCOMPRESSIONOPTION_FORCE_DWORD



