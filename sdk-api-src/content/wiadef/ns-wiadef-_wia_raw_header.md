---
UID: NS:wiadef._WIA_RAW_HEADER
title: "_WIA_RAW_HEADER"
author: windows-driver-content
description: The WIA_RAW_HEADER structure defines an image in the RAW data format of a device and enables applications to use RAW format in Windows Image Acquisition (WIA) transfers.
old-location: wia\_wia_WIA_RAW_HEADER.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\structs\wia_raw_header.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: "*PWIA_RAW_HEADER, WIA_RAW_HEADER, WIA_RAW_HEADER structure [WIA], _WIA_RAW_HEADER, _wia_WIA_RAW_HEADER, wia._wia_WIA_RAW_HEADER, wiadef/WIA_RAW_HEADER"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wiadef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WIA_RAW_HEADER, *PWIA_RAW_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wiadef.h
api_name:
-	WIA_RAW_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WIA_RAW_HEADER structure


## -description


The <b>WIA_RAW_HEADER</b> structure defines an image in the RAW data format of a device and enables applications to use RAW format in Windows Image Acquisition (WIA) transfers.


## -struct-fields




### -field Tag

Type: <b>DWORD</b>

The name of the format. This must be the literal 'WRAW' (four single byte ASCII characters).


### -field Version

Type: <b>DWORD</b>

The version of the RAW format. Always use 0x00010000.


### -field HeaderSize

Type: <b>DWORD</b>

The total valid bytes in the header.


### -field XRes

Type: <b>DWORD</b>

The horizontal resolution in dots per inch.


### -field YRes

Type: <b>DWORD</b>

The vertical resolution in dots per inch.


### -field XExtent

Type: <b>DWORD</b>

The width of the image in pixels.


### -field YExtent

Type: <b>DWORD</b>

The height of the image in pixels.


### -field BytesPerLine

Type: <b>DWORD</b>

The number of bytes in a line of an uncompressed image. Use 0 when the data is compressed to signal that the number of bytes per line is unknown.


### -field BitsPerPixel

Type: <b>DWORD</b>

The total number of bits per pixel for all the pixel's channels.


### -field ChannelsPerPixel

Type: <b>DWORD</b>

The number of color channels in a pixel.


### -field DataType

Type: <b>DWORD</b>

The WIA_IPA_DATATYPE of the image. Since WIA_IPA_FORMAT is set to WiaImgFmt_RAW, this is a list of allowed values from which the application picks. 


### -field BitsPerChannel

 


### -field Compression

Type: <b>DWORD</b>

A WIA_IPA_COMPRESSION value specifying the type of compression used, if any.


### -field PhotometricInterp

Type: <b>DWORD</b>

A WIA_IPA_PHOTOMETRIC_INTERP value specifying the photometric interpretation of the image.


### -field LineOrder

Type: <b>DWORD</b>

A value representing the image line order. This is always either WIA_LINE_ORDER_TOP_TO_BOTTOM or WIA_LINE_ORDER_BOTTOM_TO_TOP. 


### -field RawDataOffset

Type: <b>DWORD</b>

The position of the raw image data in bytes, starting from position where the header ends or the position where the palette ends.


### -field RawDataSize

Type: <b>DWORD</b>

The size, in bytes, of the raw image data. 


### -field PaletteOffset

Type: <b>DWORD</b>

The position of the palette in bytes, starting from the position where the header ends or the position where the data ends. (This value is 0, if there is no palette.) 


### -field PaletteSize

Type: <b>DWORD</b>

The size, in bytes, of the palette table. (This is 0, if there is no palette.) 


#### - BitsPerChannel[8]

Type: <b>BYTE</b>

The number of bits in a channel, up to a maximum of 8.


## -remarks



Because this is not a file format, use an empty string for the WIA_IPA_FILE_EXTENSION property. 

The palette and the data can come in either order.

<b>RawDataSize</b> does not include either the header or the palette. Use this field to verify that the transfer of the image has been successful.

<b>PaletteSize</b> is bytes, not the number of entries in the palette.



