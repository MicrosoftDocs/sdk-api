---
UID: NF:mfapi.MFAverageTimePerFrameToFrameRate
title: MFAverageTimePerFrameToFrameRate function
author: windows-sdk-content
description: Calculates the frame rate, in frames per second, from the average duration of a video frame.
old-location: mf\mfaveragetimeperframetoframerate.htm
old-project: medfound
ms.assetid: 9d2ab27f-80cb-4cd9-bd7a-8f56a810bb29
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 9d2ab27f-80cb-4cd9-bd7a-8f56a810bb29, MFAverageTimePerFrameToFrameRate, MFAverageTimePerFrameToFrameRate function [Media Foundation], mf.mfaveragetimeperframetoframerate, mfapi/MFAverageTimePerFrameToFrameRate
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
tech.root: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFAverageTimePerFrameToFrameRate
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFAverageTimePerFrameToFrameRate function


## -description



Calculates the frame rate, in frames per second, from the average duration of a video frame.




## -parameters




### -param unAverageTimePerFrame [in]

The average duration of a video frame, in 100-nanosecond units.


### -param punNumerator [out]

Receives the numerator of the frame rate.


### -param punDenominator [out]

Receives the denominator of the frame rate.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



Average time per frame is used in the older <b>VIDEOINFOHEADER</b> and <b>VIDEOINFOHEADER2</b> format structures. This function provides a standard conversion so that all components in the pipeline can use consistent values, if they need to translate between the older format structures and the media type attributes used in Media Foundation.

This function uses a look-up table for certain common durations. The table is listed in the Remarks section for the <a href="https://msdn.microsoft.com/750f6920-3386-4d50-9d59-73e876b406da">MFFrameRateToAverageTimePerFrame</a> function.




## -see-also




<a href="https://msdn.microsoft.com/750f6920-3386-4d50-9d59-73e876b406da">MFFrameRateToAverageTimePerFrame</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

