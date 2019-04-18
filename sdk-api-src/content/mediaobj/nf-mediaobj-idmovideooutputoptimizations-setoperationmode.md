---
UID: NF:mediaobj.IDMOVideoOutputOptimizations.SetOperationMode
title: IDMOVideoOutputOptimizations::SetOperationMode (mediaobj.h)
author: windows-sdk-content
description: The SetOperationMode method notifies the DMO of the optimization features that are in effect.
old-location: dshow\idmovideooutputoptimizations_setoperationmode.htm
tech.root: DirectShow
ms.assetid: 07dc29aa-d3ee-409e-9fe8-0c54d2d6f759
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDMOVideoOutputOptimizations interface [DirectShow],SetOperationMode method, IDMOVideoOutputOptimizations.SetOperationMode, IDMOVideoOutputOptimizations::SetOperationMode, IDMOVideoOutputOptimizationsSetOperationMode, SetOperationMode, SetOperationMode method [DirectShow], SetOperationMode method [DirectShow],IDMOVideoOutputOptimizations interface, dshow.idmovideooutputoptimizations_setoperationmode, mediaobj/IDMOVideoOutputOptimizations::SetOperationMode
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IDMOVideoOutputOptimizations.SetOperationMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMOVideoOutputOptimizations::SetOperationMode


## -description



The <code>SetOperationMode</code> method notifies the DMO of the optimization features that are in effect.




## -parameters




### -param ulOutputStreamIndex

Zero-based index of an output stream on the DMO.


### -param dwEnabledFeatures

Bitwise combination of zero or more flags from the <a href="https://msdn.microsoft.com/en-us/library/Dd375517(v=VS.85).aspx">DMO_VIDEO_OUTPUT_STREAM_FLAGS</a> enumeration.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument

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



Before calling this method, call the <a href="https://msdn.microsoft.com/en-us/library/Dd406846(v=VS.85).aspx">IDMOVideoOutputOptimizations::QueryOperationModePreferences</a> method to determine which features the DMO requests. Then call this method to inform the DMO which of those features you are providing. If you are not providing any of them, it is not necessary to call this method. The DMO does not assume that any of them will be provided.

The application must provide all the features it has agreed to. For some features, however, the DMO might not require the feature on every sample. To determine if the DMO can dispense with any features on the next sample, call the <a href="https://msdn.microsoft.com/en-us/library/Dd406845(v=VS.85).aspx">IDMOVideoOutputOptimizations::GetCurrentSampleRequirements</a> method. In effect, this enables the DMO to waive an agreed-upon feature for one sample.

Before streaming begins, subsequent calls to this method override earlier calls. To set multiple features, you must do so in a single method call. Once streaming begins, this method returns an error. Streaming begins when the applications calls <a href="https://msdn.microsoft.com/en-us/library/Dd406959(v=VS.85).aspx">IMediaObject::ProcessInput</a> on at least one input stream.

When streaming ends, the application can renegotiate the features. Streaming ends if the application calls the <a href="https://msdn.microsoft.com/en-us/library/Dd406945(v=VS.85).aspx">IMediaObject::Flush</a> method, or if the application calls <a href="https://msdn.microsoft.com/en-us/library/Dd406944(v=VS.85).aspx">IMediaObject::Discontinuity</a> on all the input streams and then processes all of the remaining output.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd406843(v=VS.85).aspx">IDMOVideoOutputOptimizations Interface</a>
 

 

