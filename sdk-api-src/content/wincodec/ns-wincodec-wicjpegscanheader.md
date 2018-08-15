---
UID: NS:wincodec.WICJpegScanHeader
title: WICJpegScanHeader
author: windows-sdk-content
description: Represents a JPEG frame header.
old-location: wic\wicjpegscanheader.htm
old-project: wic
ms.assetid: 87A36F9B-CD6B-4343-AAA7-9FDBAD41E38A
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WICJpegScanHeader, WICJpegScanHeader structure [Windows Imaging Component], wic.wicjpegscanheader, wincodec/WICJpegScanHeader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincodec.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WICJpegScanHeader
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wincodec.h
api_name:
 - WICJpegScanHeader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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

The format of the quantization table indices. Use one of the following constants, described in <a href="https://msdn.microsoft.com/6C0139F3-DA3E-4D7C-80D5-BC8C2D76C6A9">IWICJpegFrameDecode Constants</a>.

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



Get the scan header for an image by calling <a href="https://msdn.microsoft.com/FD434498-CC04-4702-ACD3-EDD1DDE0B3AA">IWICJpegFrameDecode::GetScanHeader</a>.



