---
UID: NS:audiomediatype._UNCOMPRESSEDAUDIOFORMAT
title: UNCOMPRESSEDAUDIOFORMAT (audiomediatype.h)
description: The UNCOMPRESSEDAUDIOFORMAT structure specifies the frame rate, channel mask, and other attributes of the uncompressed audio data format.
helpviewer_keywords: ["UNCOMPRESSEDAUDIOFORMAT","UNCOMPRESSEDAUDIOFORMAT structure [Audio Devices]","aud-prop_077921c9-89ee-44ca-a585-d87e4d025c16.xml","audio.uncompressedauudioformat","audiomediatype/UNCOMPRESSEDAUUDIOFORMAT"]
old-location: audio\uncompressedauudioformat.htm
tech.root: audio
ms.assetid: b1d35067-7ef3-4c29-8b16-642300485695
ms.date: 12/05/2018
ms.keywords: UNCOMPRESSEDAUDIOFORMAT, UNCOMPRESSEDAUDIOFORMAT structure [Audio Devices], aud-prop_077921c9-89ee-44ca-a585-d87e4d025c16.xml, audio.uncompressedauudioformat, audiomediatype/UNCOMPRESSEDAUUDIOFORMAT
req.header: audiomediatype.h
req.include-header: Audiomediatype.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UNCOMPRESSEDAUDIOFORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _UNCOMPRESSEDAUDIOFORMAT
 - audiomediatype/_UNCOMPRESSEDAUDIOFORMAT
 - UNCOMPRESSEDAUDIOFORMAT
 - audiomediatype/UNCOMPRESSEDAUDIOFORMAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Audiomediatype.h
api_name:
 - UNCOMPRESSEDAUDIOFORMAT
---

# UNCOMPRESSEDAUDIOFORMAT structure


## -description

The UNCOMPRESSEDAUDIOFORMAT structure specifies the frame rate, channel mask, and other attributes of the uncompressed audio data format.

## -struct-fields

### -field guidFormatType

Specifies the GUID of the data format type.

### -field dwSamplesPerFrame

Specifies the number of samples per frame.

### -field dwBytesPerSampleContainer

Specifies the number of bytes that make up a unit container of the sample.

### -field dwValidBitsPerSample

Specifies the number of valid bits per sample.

### -field fFramesPerSecond

Specifies the number of frames per second of streaming audio data.

### -field dwChannelMask

Specifies the channel mask that is used by the uncompressed audio data.

## -remarks

This structure provides access to the parameters that describe an uncompressed PCM audio format.

