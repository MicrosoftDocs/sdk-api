---
UID: NS:wincodec.WICJpegFrameHeader
title: WICJpegFrameHeader
author: windows-driver-content
description: Represents a JPEG frame header.
old-location: wic\wicjpegframeheader.htm
old-project: wic
ms.assetid: BB207D78-9E27-49A4-91E4-601CED109389
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: WICJpegFrameHeader, WICJpegFrameHeader structure [Windows Imaging Component], wic.wicjpegframeheader, wincodec/WICJpegFrameHeader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICJpegFrameHeader
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wincodec.h
api_name:
-	WICJpegFrameHeader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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

The sample factors. Use one of the following constants, described in <a href="https://msdn.microsoft.com/6C0139F3-DA3E-4D7C-80D5-BC8C2D76C6A9">IWICJpegFrameDecode Constants</a>.

<ul>
<li>WIC_JPEG_SAMPLE_FACTORS_ONE</li>
<li>WIC_JPEG_SAMPLE_FACTORS_THREE_420</li>
<li>WIC_JPEG_SAMPLE_FACTORS_THREE_422</li>
<li>WIC_JPEG_SAMPLE_FACTORS_THREE_440</li>
<li>WIC_JPEG_SAMPLE_FACTORS_THREE_444</li>
</ul>

### -field QuantizationTableIndices

The format of the quantization table indices. Use one of the following constants, described in <a href="https://msdn.microsoft.com/6C0139F3-DA3E-4D7C-80D5-BC8C2D76C6A9">IWICJpegFrameDecode Constants</a>.

<ul>
<li>WIC_JPEG_QUANTIZATION_BASELINE_ONE</li>
<li>WIC_JPEG_QUANTIZATION_BASELINE_THREE </li>
</ul>

## -remarks



Get the frame header for an image by calling <a href="https://msdn.microsoft.com/CE29251F-C2E2-422B-B6BD-034D6B479009">IWICJpegFrameDecode::GetFrameHeader</a>.




## -see-also




<a href="https://msdn.microsoft.com/CE29251F-C2E2-422B-B6BD-034D6B479009">IWICJpegFrameDecode::GetFrameHeader</a>
 

 

