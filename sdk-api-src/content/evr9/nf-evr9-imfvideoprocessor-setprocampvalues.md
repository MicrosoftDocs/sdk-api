---
UID: NF:evr9.IMFVideoProcessor.SetProcAmpValues
title: IMFVideoProcessor::SetProcAmpValues (evr9.h)
description: Sets one or more color adjustment (ProcAmp) settings.
helpviewer_keywords: ["84a5e022-773c-483b-adb5-5883b25b716f","IMFVideoProcessor interface [Media Foundation]","SetProcAmpValues method","IMFVideoProcessor.SetProcAmpValues","IMFVideoProcessor::SetProcAmpValues","SetProcAmpValues","SetProcAmpValues method [Media Foundation]","SetProcAmpValues method [Media Foundation]","IMFVideoProcessor interface","evr9/IMFVideoProcessor::SetProcAmpValues","mf.imfvideoprocessor_setprocampvalues"]
old-location: mf\imfvideoprocessor_setprocampvalues.htm
tech.root: mf
ms.assetid: 84a5e022-773c-483b-adb5-5883b25b716f
ms.date: 12/05/2018
ms.keywords: 84a5e022-773c-483b-adb5-5883b25b716f, IMFVideoProcessor interface [Media Foundation],SetProcAmpValues method, IMFVideoProcessor.SetProcAmpValues, IMFVideoProcessor::SetProcAmpValues, SetProcAmpValues, SetProcAmpValues method [Media Foundation], SetProcAmpValues method [Media Foundation],IMFVideoProcessor interface, evr9/IMFVideoProcessor::SetProcAmpValues, mf.imfvideoprocessor_setprocampvalues
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoProcessor::SetProcAmpValues
 - evr9/IMFVideoProcessor::SetProcAmpValues
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoProcessor.SetProcAmpValues
---

# IMFVideoProcessor::SetProcAmpValues


## -description

Sets one or more color adjustment (ProcAmp) settings.

## -parameters

### -param dwFlags [in]

Bitwise <b>OR</b> of one or more flags, specifying which ProcAmp values to set. For a list of flags, see <a href="/windows/desktop/medfound/procamp-settings">ProcAmp Settings</a>.

### -param pValues [in]

Pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_procampvalues">DXVA2_ProcAmpValues</a> structure. For each flag that you set in <i>dwFlags</i>, set the corresponding structure member to the desired value. To get the valid range of values for each operation, call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocamprange">IMFVideoProcessor::GetProcAmpRange</a>. The method ignores any structure members for which the corresponding flag is not set in <i>dwFlags</i>.

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

Before calling this method, set the video processor mode. To select a video processor mode, call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode">IMFVideoProcessor::SetVideoProcessorMode</a>. Otherwise, the EVR automatically selects a mode when streaming begins.

To find out which ProcAmp settings the driver supports, call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps">IMFVideoProcessor::GetVideoProcessorCaps</a>.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor">IMFVideoProcessor</a>