---
UID: NF:evr9.IMFVideoProcessor.GetFilteringValue
title: IMFVideoProcessor::GetFilteringValue
author: windows-sdk-content
description: Retrieves the current setting for an image filter.
old-location: mf\imfvideoprocessor_getfilteringvalue.htm
tech.root: medfound
ms.assetid: 1c8d6836-ca62-4d26-be4e-572dc6ff994d
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 1c8d6836-ca62-4d26-be4e-572dc6ff994d, GetFilteringValue, GetFilteringValue method [Media Foundation], GetFilteringValue method [Media Foundation],IMFVideoProcessor interface, IMFVideoProcessor interface [Media Foundation],GetFilteringValue method, IMFVideoProcessor.GetFilteringValue, IMFVideoProcessor::GetFilteringValue, evr9/IMFVideoProcessor::GetFilteringValue, mf.imfvideoprocessor_getfilteringvalue
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
 - IMFVideoProcessor.GetFilteringValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoProcessor::GetFilteringValue


## -description



Retrieves the current setting for an image filter.




## -parameters




### -param dwProperty [in]

The filter setting to query. For a list of possible values, see <a href="https://msdn.microsoft.com/6514992e-8188-4d28-879c-547e9b340b28">DXVA Image Filter Settings</a>.


### -param pValue [out]

Pointer to a <a href="https://msdn.microsoft.com/5f8f4515-1cf4-4060-813b-c746649c5c40">DXVA2_Fixed32</a> structure that receives the current value.


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



Before calling this method, you must set the media type for the reference stream.

Until the mixer's video processor mode is set, the returned values are all zero. After the processor mode is set, the returned values reflect the current mode. To select a video processor mode, call <a href="https://msdn.microsoft.com/4b353576-c8ee-4f73-9ee6-ba4545a6f4fc">IMFVideoProcessor::SetVideoProcessorMode</a>. Otherwise, the EVR automatically selects a mode when streaming begins.

To find out which image filters the driver supports, call <a href="https://msdn.microsoft.com/9a02aed2-8225-4416-ae54-7ed51c67a149">IMFVideoProcessor::GetVideoProcessorCaps</a>.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/0a63c4f8-eb32-4f0c-b69b-0c16243f2f21">IMFVideoProcessor</a>
 

 

