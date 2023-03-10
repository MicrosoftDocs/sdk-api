---
UID: NS:wincodec.WICJpegScanHeader
title: WICJpegScanHeader (wincodec.h)
description: Represents a JPEG frame header. (WICJpegScanHeader)
helpviewer_keywords: ["WICJpegScanHeader","WICJpegScanHeader structure [Windows Imaging Component]","wic.wicjpegscanheader","wincodec/WICJpegScanHeader"]
old-location: wic\wicjpegscanheader.htm
tech.root: wic
ms.assetid: 87A36F9B-CD6B-4343-AAA7-9FDBAD41E38A
ms.date: 12/05/2018
ms.keywords: WICJpegScanHeader, WICJpegScanHeader structure [Windows Imaging Component], wic.wicjpegscanheader, wincodec/WICJpegScanHeader
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
targetos: Windows
req.typenames: WICJpegScanHeader
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICJpegScanHeader
 - wincodec/WICJpegScanHeader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wincodec.h
api_name:
 - WICJpegScanHeader
---

# WICJpegScanHeader structure


## -description

Represents a JPEG frame header.

## -struct-fields

### -field cComponents

The number of components in the scan.

### -field RestartInterval

The interval of reset markers within the scan.

### -field ComponentSelectors

The component identifiers.

### -field HuffmanTableIndices

The format of the quantization table indices. Use one of the following constants, described in <a href="/windows/desktop/wic/iwicjpegframedecode-constants">IWICJpegFrameDecode Constants</a>.

<ul>
<li>WIC_JPEG_HUFFMAN_BASELINE_ONE</li>
<li>WIC_JPEG_HUFFMAN_BASELINE_THREE </li>
</ul>

### -field StartSpectralSelection

The start of the spectral selection.

### -field EndSpectralSelection

The end of the spectral selection.

### -field SuccessiveApproximationHigh

The successive approximation high.

### -field SuccessiveApproximationLow

The successive approximation low.

## -remarks

Get the scan header for an image by calling <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-getscanheader">IWICJpegFrameDecode::GetScanHeader</a>.
