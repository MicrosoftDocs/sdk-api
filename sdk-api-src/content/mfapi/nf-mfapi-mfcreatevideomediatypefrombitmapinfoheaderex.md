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

# MFCreateVideoMediaTypeFromBitMapInfoHeaderEx function


## -description


Creates a video media type from a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure.


## -parameters




### -param pbmihBitMapInfoHeader [in]

A pointer to the <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure to convert.


### -param cbBitMapInfoHeader [in]

The size of the <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure in bytes, including the size of any palette entries or color masks that follow the structure.


### -param dwPixelAspectRatioX

The X dimension of the pixel aspect ratio.


### -param dwPixelAspectRatioY

The Y dimension of the pixel aspect ratio.


### -param InterlaceMode

A member of the <a href="https://msdn.microsoft.com/10a3d7b1-74ed-46cd-b10e-59a8f01726d5">MFVideoInterlaceMode</a> enumeration, specifying how the video is interlaced.


### -param VideoFlags

A bitwise <b>OR</b> of flags from the <a href="https://msdn.microsoft.com/2530bf1d-05b1-4c16-b00b-117c0dadb301">MFVideoFlags</a> enumeration.


### -param dwFramesPerSecondNumerator

The numerator of the 
          frame rate in frames per second.


### -param dwFramesPerSecondDenominator

The denominator of the frame rate in frames per second


### -param dwMaxBitRate

The approximate data rate of the video stream, in bits per second. If the rate is unknown, set this parameter to zero.
          


### -param ppIVideoMediaType [out]

Receives a pointer to the 
          <a href="https://msdn.microsoft.com/9109b0dd-c44d-41d4-9480-1ca5c667dbd7">IMFVideoMediaType</a> interface. The caller must release the interface.


## -returns



If the function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

