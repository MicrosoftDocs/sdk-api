---
UID: NF:mfapi.MFFrameRateToAverageTimePerFrame
title: MFFrameRateToAverageTimePerFrame function (mfapi.h)
description: Converts a video frame rate into a frame duration.
helpviewer_keywords: ["750f6920-3386-4d50-9d59-73e876b406da","MFFrameRateToAverageTimePerFrame","MFFrameRateToAverageTimePerFrame function [Media Foundation]","mf.mfframeratetoaveragetimeperframe","mfapi/MFFrameRateToAverageTimePerFrame"]
old-location: mf\mfframeratetoaveragetimeperframe.htm
tech.root: mf
ms.assetid: 750f6920-3386-4d50-9d59-73e876b406da
ms.date: 12/05/2018
ms.keywords: 750f6920-3386-4d50-9d59-73e876b406da, MFFrameRateToAverageTimePerFrame, MFFrameRateToAverageTimePerFrame function [Media Foundation], mf.mfframeratetoaveragetimeperframe, mfapi/MFFrameRateToAverageTimePerFrame
req.header: mfapi.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFFrameRateToAverageTimePerFrame
 - mfapi/MFFrameRateToAverageTimePerFrame
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFFrameRateToAverageTimePerFrame
---

# MFFrameRateToAverageTimePerFrame function


## -description

Converts a video frame rate into a frame duration.

## -parameters

### -param unNumerator [in]

The numerator of the frame rate.

### -param unDenominator [in]

The denominator of the frame rate.

### -param punAverageTimePerFrame [out]

Receives the average duration of a video frame, in 100-nanosecond units.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is useful for calculating time stamps on a sample, given the frame rate.

Also, average time per frame is used in the older <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> and <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2">VIDEOINFOHEADER2</a> format structures. This function provides a standard conversion so that all components in the pipeline can use consistent values, if they need to translate between the older format structures and the media type attributes used in Media Foundation.

For certain common frame rates, the function gets the frame duration from a look-up table:

<table>
<tr>
<th>Frames per second (floating point)</th>
<th>Frames per second (fractional)</th>
<th>Average time per frame</th>
</tr>
<tr>
<td>59.94</td>
<td>60000/1001</td>
<td>166833</td>
</tr>
<tr>
<td>29.97</td>
<td>30000/1001</td>
<td>333667</td>
</tr>
<tr>
<td>23.976</td>
<td>24000/1001</td>
<td>417188</td>
</tr>
<tr>
<td>60</td>
<td>60/1</td>
<td>166667</td>
</tr>
<tr>
<td>30</td>
<td>30/1</td>
<td>333333</td>
</tr>
<tr>
<td>50</td>
<td>50/1</td>
<td>200000</td>
</tr>
<tr>
<td>25</td>
<td>25/1</td>
<td>400000</td>
</tr>
<tr>
<td>24</td>
<td>24/1</td>
<td>416667</td>
</tr>
</table>
 

Most video content uses one of the frame rates listed here.
      For other frame rates, the function calculates the duration.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate">MFAverageTimePerFrameToFrameRate</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>