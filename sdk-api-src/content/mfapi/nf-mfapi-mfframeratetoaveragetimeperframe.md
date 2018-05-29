---
UID: NF:mfapi.MFFrameRateToAverageTimePerFrame
title: MFFrameRateToAverageTimePerFrame function
author: windows-sdk-content
description: Converts a video frame rate into a frame duration.
old-location: mf\mfframeratetoaveragetimeperframe.htm
old-project: medfound
ms.assetid: 750f6920-3386-4d50-9d59-73e876b406da
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 750f6920-3386-4d50-9d59-73e876b406da, MFFrameRateToAverageTimePerFrame, MFFrameRateToAverageTimePerFrame function [Media Foundation], mf.mfframeratetoaveragetimeperframe, mfapi/MFFrameRateToAverageTimePerFrame
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFFrameRateToAverageTimePerFrame
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
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



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is useful for calculating time stamps on a sample, given the frame rate.

Also, average time per frame is used in the older <a href="https://msdn.microsoft.com/a175592b-0dc1-4001-b52f-785407965932">VIDEOINFOHEADER</a> and <a href="https://msdn.microsoft.com/5e3d5bf0-435f-45da-8409-a1463b56a7ae">VIDEOINFOHEADER2</a> format structures. This function provides a standard conversion so that all components in the pipeline can use consistent values, if they need to translate between the older format structures and the media type attributes used in Media Foundation.


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




<a href="https://msdn.microsoft.com/9d2ab27f-80cb-4cd9-bd7a-8f56a810bb29">MFAverageTimePerFrameToFrameRate</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

