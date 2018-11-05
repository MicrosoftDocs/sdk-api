---
UID: NF:mfapi.MFCreateVideoMediaTypeFromBitMapInfoHeaderEx
title: MFCreateVideoMediaTypeFromBitMapInfoHeaderEx function
author: windows-sdk-content
description: Creates a video media type from a BITMAPINFOHEADER structure.
old-location: mf\mfcreatevideomediatypefrombitmapinfoheaderex.htm
tech.root: medfound
ms.assetid: 27160995-e934-4050-a231-d69d4f75dfce
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: MFCreateVideoMediaTypeFromBitMapInfoHeaderEx, MFCreateVideoMediaTypeFromBitMapInfoHeaderEx function [Media Foundation], mf.mfcreatevideomediatypefrombitmapinfoheaderex, mfapi/MFCreateVideoMediaTypeFromBitMapInfoHeaderEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Evr.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateVideoMediaTypeFromBitMapInfoHeaderEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

