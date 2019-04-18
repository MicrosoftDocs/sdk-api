---
UID: NF:evr9.IMFVideoProcessor.GetProcAmpValues
title: IMFVideoProcessor::GetProcAmpValues (evr9.h)
author: windows-sdk-content
description: Retrieves the current settings for one or more color adjustment (ProcAmp) settings.
old-location: mf\imfvideoprocessor_getprocampvalues.htm
tech.root: medfound
ms.assetid: d1d6f6a4-fe3b-4acf-a004-d02ece41a302
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetProcAmpValues, GetProcAmpValues method [Media Foundation], GetProcAmpValues method [Media Foundation],IMFVideoProcessor interface, IMFVideoProcessor interface [Media Foundation],GetProcAmpValues method, IMFVideoProcessor.GetProcAmpValues, IMFVideoProcessor::GetProcAmpValues, d1d6f6a4-fe3b-4acf-a004-d02ece41a302, evr9/IMFVideoProcessor::GetProcAmpValues, mf.imfvideoprocessor_getprocampvalues
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoProcessor.GetProcAmpValues
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoProcessor::GetProcAmpValues


## -description



Retrieves the current settings for one or more color adjustment (ProcAmp) settings.




## -parameters




### -param dwFlags [in]

Bitwise <b>OR</b> of one or more flags, specifying which operations to query. For a list of flags, see <a href="https://msdn.microsoft.com/60d97b9e-d77c-4e53-94ea-ebd59c2601df">ProcAmp Settings</a>.


### -param Values [out]

Pointer to a <a href="https://msdn.microsoft.com/c84acd34-e922-46bb-9913-0f94c7c47155">DXVA2_ProcAmpValues</a> structure. The method fills the structure with the current value of each operation specified in <i>dwFlags</i>.


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
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The media type for the reference stream is not set.

</td>
</tr>
</table>
 




## -remarks



Before calling this method, you must set the media type for the reference stream.

Until the mixer's video processor mode is set, the returned values are all zero. After the processor mode is set, the returned values reflect the current mode. To select a video processor mode, call <a href="https://msdn.microsoft.com/4b353576-c8ee-4f73-9ee6-ba4545a6f4fc">IMFVideoProcessor::SetVideoProcessorMode</a>. Otherwise, the EVR automatically selects a mode when streaming begins.

To find out which ProcAmp settings the driver supports, call <a href="https://msdn.microsoft.com/9a02aed2-8225-4416-ae54-7ed51c67a149">IMFVideoProcessor::GetVideoProcessorCaps</a>.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/0a63c4f8-eb32-4f0c-b69b-0c16243f2f21">IMFVideoProcessor</a>
 

 

