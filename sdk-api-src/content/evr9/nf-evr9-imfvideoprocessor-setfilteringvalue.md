---
UID: NF:evr9.IMFVideoProcessor.SetFilteringValue
title: IMFVideoProcessor::SetFilteringValue
author: windows-sdk-content
description: Sets a parameter for an image filter.
old-location: mf\imfvideoprocessor_setfilteringvalue.htm
tech.root: MedFound
ms.assetid: cb3c9516-2083-4c9d-b583-fc561f977ed5
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IMFVideoProcessor interface [Media Foundation],SetFilteringValue method, IMFVideoProcessor.SetFilteringValue, IMFVideoProcessor::SetFilteringValue, SetFilteringValue, SetFilteringValue method [Media Foundation], SetFilteringValue method [Media Foundation],IMFVideoProcessor interface, cb3c9516-2083-4c9d-b583-fc561f977ed5, evr9/IMFVideoProcessor::SetFilteringValue, mf.imfvideoprocessor_setfilteringvalue
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
 - IMFVideoProcessor.SetFilteringValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoProcessor::SetFilteringValue


## -description



Sets a parameter for an image filter.




## -parameters




### -param dwProperty [in]

The image filtering parameter to set. For a list of possible values, see <a href="https://msdn.microsoft.com/6514992e-8188-4d28-879c-547e9b340b28">DXVA Image Filter Settings</a>.


### -param pValue [in]

Pointer to a <a href="https://msdn.microsoft.com/5f8f4515-1cf4-4060-813b-c746649c5c40">DXVA2_Fixed32</a> structure that specifies the new value. To get the valid range of values for each parameter, call <a href="https://msdn.microsoft.com/1e5f1635-51fe-4394-8a25-dcee3f55c711">IMFVideoProcessor::GetFilteringRange</a>.


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
The value of <i>dwProperty</i> is invalid.

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

To find out which image filters the driver supports, call <a href="https://msdn.microsoft.com/9a02aed2-8225-4416-ae54-7ed51c67a149">IMFVideoProcessor::GetVideoProcessorCaps</a>.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/0a63c4f8-eb32-4f0c-b69b-0c16243f2f21">IMFVideoProcessor</a>
 

 

