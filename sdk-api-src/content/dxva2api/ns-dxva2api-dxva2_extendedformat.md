---
UID: NS:dxva2api._DXVA2_ExtendedFormat
title: DXVA2_ExtendedFormat (dxva2api.h)
description: Describes the format of a video stream.
helpviewer_keywords: ["DXVA2_ExtendedFormat","DXVA2_ExtendedFormat structure [Media Foundation]","dxva2api/DXVA2_ExtendedFormat","eba2c56b-8951-4dc5-91ae-1371793ce787","mf.dxva2_extendedformat"]
old-location: mf\dxva2_extendedformat.htm
tech.root: mf
ms.assetid: eba2c56b-8951-4dc5-91ae-1371793ce787
ms.date: 12/05/2018
ms.keywords: DXVA2_ExtendedFormat, DXVA2_ExtendedFormat structure [Media Foundation], dxva2api/DXVA2_ExtendedFormat, eba2c56b-8951-4dc5-91ae-1371793ce787, mf.dxva2_extendedformat
req.header: dxva2api.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DXVA2_ExtendedFormat
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA2_ExtendedFormat
 - dxva2api/_DXVA2_ExtendedFormat
 - DXVA2_ExtendedFormat
 - dxva2api/DXVA2_ExtendedFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva2api.h
api_name:
 - DXVA2_ExtendedFormat
---

# DXVA2_ExtendedFormat structure


## -description

Describes the format of a video stream.

## -struct-fields

### -field SampleFormat

Describes the interlacing of the video frames. Contains a value from the <a href="/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat">DXVA2_SampleFormat</a> enumeration.

### -field VideoChromaSubsampling

Describes the chroma siting. Contains a value from the <a href="/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_videochromasubsampling">DXVA2_VideoChromaSubSampling</a> enumeration.

### -field NominalRange

Describes the nominal range of the Y'CbCr or RGB color data. Contains a value from the <a href="/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_nominalrange">DXVA2_NominalRange</a> enumeration.

### -field VideoTransferMatrix

Describes the transform from Y'PbPr (component video) to studio R'G'B'. Contains a value from the <a href="/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_videotransfermatrix">DXVA2_VideoTransferMatrix</a> enumeration.

### -field VideoLighting

Describes the intended viewing conditions. Contains a value from the <a href="/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_videolighting">DXVA2_VideoLighting</a> enumeration.

### -field VideoPrimaries

Describes the color primaries. Contains a value from the <a href="/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_videoprimaries">DXVA2_VideoPrimaries</a> enumeration.

### -field VideoTransferFunction

Describes the gamma correction transfer function. Contains a value from the <a href="/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_videotransferfunction">DXVA2_VideoTransferFunction</a> enumeration.

### -field value

Use this member to access all of the bits in the union.

## -remarks

Most of the values in this structure can be translated directly to and from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> attributes. For a code example that fills in the values from an <b>IMFMediaType</b> pointer, see <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc">DXVA2_VideoDesc</a>.

## -see-also

<a href="/windows/desktop/medfound/extended-color-information">Extended Color Information</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>