---
UID: NF:evr9.IMFVideoProcessor.GetAvailableVideoProcessorModes
title: IMFVideoProcessor::GetAvailableVideoProcessorModes
author: windows-sdk-content
description: Retrieves the video processor modes that the video driver supports.
old-location: mf\imfvideoprocessor_getavailablevideoprocessormodes.htm
old-project: medfound
ms.assetid: 1004341d-d39b-4032-a027-39e35ecab635
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: 1004341d-d39b-4032-a027-39e35ecab635, GetAvailableVideoProcessorModes, GetAvailableVideoProcessorModes method [Media Foundation], GetAvailableVideoProcessorModes method [Media Foundation],IMFVideoProcessor interface, IMFVideoProcessor interface [Media Foundation],GetAvailableVideoProcessorModes method, IMFVideoProcessor.GetAvailableVideoProcessorModes, IMFVideoProcessor::GetAvailableVideoProcessorModes, evr9/IMFVideoProcessor::GetAvailableVideoProcessorModes, mf.imfvideoprocessor_getavailablevideoprocessormodes
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFVideoAlphaBitmapFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoProcessor.GetAvailableVideoProcessorModes
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoProcessor::GetAvailableVideoProcessorModes


## -description



Retrieves the video processor modes that the video driver supports.




## -parameters




### -param lpdwNumProcessingModes [in, out]

Receives the number of video processor modes.


### -param ppVideoProcessingModes [out]

Receives a pointer to an array of GUIDs. The number of elements in the array is returned in the <i>lpdwNumProcessingModes</i> parameter. The caller must release the memory for the array by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. This parameter can be <b>NULL</b>.


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



Video processor modes are identified by GUID. For a list of predefined GUIDs, see <a href="https://msdn.microsoft.com/26b52407-7c75-4731-aff3-41376aa9ac3a">IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids</a>. A driver can define additional vendor-specific GUIDs. To get the capabilities of each mode, pass the GUID to the <a href="https://msdn.microsoft.com/9a02aed2-8225-4416-ae54-7ed51c67a149">IMFVideoProcessor::GetVideoProcessorCaps</a> method.

Before calling this method, you must set the media type for the reference stream. Which modes are available might depend on the media type of the reference stream.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/0a63c4f8-eb32-4f0c-b69b-0c16243f2f21">IMFVideoProcessor</a>
 

 

