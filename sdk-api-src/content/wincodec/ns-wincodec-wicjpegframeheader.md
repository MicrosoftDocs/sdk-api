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
 

 

