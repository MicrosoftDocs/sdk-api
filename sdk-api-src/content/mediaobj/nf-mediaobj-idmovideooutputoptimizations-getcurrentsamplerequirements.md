---
UID: NF:mediaobj.IDMOVideoOutputOptimizations.GetCurrentSampleRequirements
title: IDMOVideoOutputOptimizations::GetCurrentSampleRequirements (mediaobj.h)
description: The GetCurrentSampleRequirements method retrieves the optimization features required to process the next sample, given the features already agreed to by the application.
helpviewer_keywords: ["GetCurrentSampleRequirements","GetCurrentSampleRequirements method [DirectShow]","GetCurrentSampleRequirements method [DirectShow]","IDMOVideoOutputOptimizations interface","IDMOVideoOutputOptimizations interface [DirectShow]","GetCurrentSampleRequirements method","IDMOVideoOutputOptimizations.GetCurrentSampleRequirements","IDMOVideoOutputOptimizations::GetCurrentSampleRequirements","IDMOVideoOutputOptimizationsGetCurrentSampleRequirements","dshow.idmovideooutputoptimizations_getcurrentsamplerequirements","mediaobj/IDMOVideoOutputOptimizations::GetCurrentSampleRequirements"]
old-location: dshow\idmovideooutputoptimizations_getcurrentsamplerequirements.htm
tech.root: dshow
ms.assetid: 95acde54-2bdb-4a80-b078-d98945604c7e
ms.date: 12/05/2018
ms.keywords: GetCurrentSampleRequirements, GetCurrentSampleRequirements method [DirectShow], GetCurrentSampleRequirements method [DirectShow],IDMOVideoOutputOptimizations interface, IDMOVideoOutputOptimizations interface [DirectShow],GetCurrentSampleRequirements method, IDMOVideoOutputOptimizations.GetCurrentSampleRequirements, IDMOVideoOutputOptimizations::GetCurrentSampleRequirements, IDMOVideoOutputOptimizationsGetCurrentSampleRequirements, dshow.idmovideooutputoptimizations_getcurrentsamplerequirements, mediaobj/IDMOVideoOutputOptimizations::GetCurrentSampleRequirements
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDMOVideoOutputOptimizations::GetCurrentSampleRequirements
 - mediaobj/IDMOVideoOutputOptimizations::GetCurrentSampleRequirements
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IDMOVideoOutputOptimizations.GetCurrentSampleRequirements
---

# IDMOVideoOutputOptimizations::GetCurrentSampleRequirements


## -description

The <code>GetCurrentSampleRequirements</code> method retrieves the optimization features required to process the next sample, given the features already agreed to by the application.

## -parameters

### -param ulOutputStreamIndex

Zero-based index of an output stream on the DMO.

### -param pdwRequestedFeatures

Pointer to a variable that receives the required features. The returned value is a bitwise combination of zero or more flags from the <a href="/windows/desktop/api/mediaobj/ne-mediaobj-_dmo_video_output_stream_flags">DMO_VIDEO_OUTPUT_STREAM_FLAGS</a> enumeration.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_INVALIDSTREAMINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

After an application calls the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-idmovideooutputoptimizations-setoperationmode">IDMOVideoOutputOptimizations::SetOperationMode</a> method, it must provide all the features it has agreed to. However, the DMO might not require every feature on every sample. This method enables the DMO to waive an agreed-upon feature for one sample.

Before processing a sample, the application can call this method. If the DMO does not require a given feature in order to process the next sample, it omits the corresponding flag from the <i>pdwRequestedFeatures</i> parameter. For the next sample only, the application can ignore the feature. The results of this method are valid only for the next call to the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput">IMediaObject::ProcessOutput</a> method.

The DMO will return only the flags that were agreed to in the <b>SetOperationMode</b> method. In other words, you cannot dynamically enable new features with this method.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-idmovideooutputoptimizations">IDMOVideoOutputOptimizations Interface</a>