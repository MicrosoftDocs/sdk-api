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



