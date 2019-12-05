---
UID: NS:wincodec.WICJpegFrameHeader
title: WICJpegFrameHeader (wincodec.h)
description: Represents a JPEG frame header.
old-location: wic\wicjpegframeheader.htm
tech.root: wic
ms.assetid: BB207D78-9E27-49A4-91E4-601CED109389
ms.date: 12/05/2018
ms.keywords: WICJpegFrameHeader, WICJpegFrameHeader structure [Windows Imaging Component], wic.wicjpegframeheader, wincodec/WICJpegFrameHeader
ms.topic: struct
f1_keywords:
- wincodec/WICJpegFrameHeader
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- wincodec.h
api_name:
- WICJpegFrameHeader
targetos: Windows
req.typenames: WICJpegFrameHeader
req.redist: 
ms.custom: 19H1
---

# WICJpegFrameHeader structure


## -description


Represents a JPEG frame header.


## -struct-fields




### -field Width

The width of the JPEG frame.


### -field Height

The height of the JPEG frame.


### -field TransferMatrix

The transfer matrix of the JPEG frame.


### -field ScanType

The scan type of the JPEG frame.


### -field cComponents

The number of components in the frame.


### -field ComponentIdentifiers

The component identifiers.


### -field SampleFactors

The sample factors. Use one of the following constants, described in <a href="https://docs.microsoft.com/windows/desktop/wic/iwicjpegframedecode-constants">IWICJpegFrameDecode Constants</a>.

<ul>
<li>WIC_JPEG_SAMPLE_FACTORS_ONE</li>
<li>WIC_JPEG_SAMPLE_FACTORS_THREE_420</li>
<li>WIC_JPEG_SAMPLE_FACTORS_THREE_422</li>
<li>WIC_JPEG_SAMPLE_FACTORS_THREE_440</li>
<li>WIC_JPEG_SAMPLE_FACTORS_THREE_444</li>
</ul>

### -field QuantizationTableIndices

The format of the quantization table indices. Use one of the following constants, described in <a href="https://docs.microsoft.com/windows/desktop/wic/iwicjpegframedecode-constants">IWICJpegFrameDecode Constants</a>.

<ul>
<li>WIC_JPEG_QUANTIZATION_BASELINE_ONE</li>
<li>WIC_JPEG_QUANTIZATION_BASELINE_THREE </li>
</ul>

## -remarks



Get the frame header for an image by calling <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-getframeheader">IWICJpegFrameDecode::GetFrameHeader</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-getframeheader">IWICJpegFrameDecode::GetFrameHeader</a>
 

 

