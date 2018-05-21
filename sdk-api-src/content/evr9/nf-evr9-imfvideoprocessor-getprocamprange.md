---
UID: NF:evr9.IMFVideoProcessor.GetProcAmpRange
title: IMFVideoProcessor::GetProcAmpRange
author: windows-driver-content
description: Retrieves the range of values for a color adjustment (ProcAmp) setting.
old-location: mf\imfvideoprocessor_getprocamprange.htm
old-project: medfound
ms.assetid: 03894bfe-020a-4478-af6f-88521d4bbb6d
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: 03894bfe-020a-4478-af6f-88521d4bbb6d, GetProcAmpRange, GetProcAmpRange method [Media Foundation], GetProcAmpRange method [Media Foundation],IMFVideoProcessor interface, IMFVideoProcessor interface [Media Foundation],GetProcAmpRange method, IMFVideoProcessor.GetProcAmpRange, IMFVideoProcessor::GetProcAmpRange, evr9/IMFVideoProcessor::GetProcAmpRange, mf.imfvideoprocessor_getprocamprange
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
-	IMFVideoProcessor.GetProcAmpRange
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoProcessor::GetProcAmpRange


## -description



Retrieves the range of values for a color adjustment (ProcAmp) setting.




## -parameters




### -param dwProperty [in]

The ProcAmp setting to query. For a list of possible values, see <a href="https://msdn.microsoft.com/60d97b9e-d77c-4e53-94ea-ebd59c2601df">ProcAmp Settings</a>.


### -param pPropRange [out]

Pointer to a <a href="https://msdn.microsoft.com/e01328bb-9069-4874-aa35-b3c9bc1c6094">DXVA2_ValueRange</a> structure that receives range of values for the specified ProcAmp setting.


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
Invalid value for <i>dwProperty</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
No video processor mode has been set.

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



This method returns the range of values that the current video processor mode supports for the specified ProcAmp setting.

This method fails if the video processor mode has not been set on the mixer. To select a video processor mode, call <a href="https://msdn.microsoft.com/4b353576-c8ee-4f73-9ee6-ba4545a6f4fc">IMFVideoProcessor::SetVideoProcessorMode</a>. Otherwise, the EVR automatically selects a mode when streaming begins.

To find out which ProcAmp settings the driver supports, call <a href="https://msdn.microsoft.com/9a02aed2-8225-4416-ae54-7ed51c67a149">IMFVideoProcessor::GetVideoProcessorCaps</a>.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/0a63c4f8-eb32-4f0c-b69b-0c16243f2f21">IMFVideoProcessor</a>
 

 

