---
UID: NF:evr9.IMFVideoProcessor.SetProcAmpValues
title: IMFVideoProcessor::SetProcAmpValues
author: windows-driver-content
description: Sets one or more color adjustment (ProcAmp) settings.
old-location: mf\imfvideoprocessor_setprocampvalues.htm
old-project: medfound
ms.assetid: 84a5e022-773c-483b-adb5-5883b25b716f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 84a5e022-773c-483b-adb5-5883b25b716f, IMFVideoProcessor interface [Media Foundation],SetProcAmpValues method, IMFVideoProcessor.SetProcAmpValues, IMFVideoProcessor::SetProcAmpValues, SetProcAmpValues, SetProcAmpValues method [Media Foundation], SetProcAmpValues method [Media Foundation],IMFVideoProcessor interface, evr9/IMFVideoProcessor::SetProcAmpValues, mf.imfvideoprocessor_setprocampvalues
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: evr9.h
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
req.typenames: MFVideoAlphaBitmapFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	strmiids.lib
-	strmiids.dll
api_name:
-	IMFVideoProcessor.SetProcAmpValues
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoProcessor::SetProcAmpValues


## -description



Sets one or more color adjustment (ProcAmp) settings.




## -parameters




### -param dwFlags [in]

Bitwise <b>OR</b> of one or more flags, specifying which ProcAmp values to set. For a list of flags, see <a href="https://msdn.microsoft.com/60d97b9e-d77c-4e53-94ea-ebd59c2601df">ProcAmp Settings</a>.


### -param pValues [in]

Pointer to a <a href="https://msdn.microsoft.com/c84acd34-e922-46bb-9913-0f94c7c47155">DXVA2_ProcAmpValues</a> structure. For each flag that you set in <i>dwFlags</i>, set the corresponding structure member to the desired value. To get the valid range of values for each operation, call <a href="https://msdn.microsoft.com/03894bfe-020a-4478-af6f-88521d4bbb6d">IMFVideoProcessor::GetProcAmpRange</a>. The method ignores any structure members for which the corresponding flag is not set in <i>dwFlags</i>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter is invalid, or one or more values in <i>pValues</i> is not within the correct range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The media type for the reference stream is not set.

</td>
</tr>
</table>
 




## -remarks



Before calling this method, set the video processor mode. To select a video processor mode, call <a href="https://msdn.microsoft.com/4b353576-c8ee-4f73-9ee6-ba4545a6f4fc">IMFVideoProcessor::SetVideoProcessorMode</a>. Otherwise, the EVR automatically selects a mode when streaming begins.

To find out which ProcAmp settings the driver supports, call <a href="https://msdn.microsoft.com/9a02aed2-8225-4416-ae54-7ed51c67a149">IMFVideoProcessor::GetVideoProcessorCaps</a>.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/0a63c4f8-eb32-4f0c-b69b-0c16243f2f21">IMFVideoProcessor</a>
 

 

