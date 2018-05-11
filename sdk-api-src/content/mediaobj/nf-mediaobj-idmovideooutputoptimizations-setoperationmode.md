---
UID: NF:mediaobj.IDMOVideoOutputOptimizations.SetOperationMode
title: IDMOVideoOutputOptimizations::SetOperationMode
author: windows-driver-content
description: The SetOperationMode method notifies the DMO of the optimization features that are in effect.
old-location: dshow\idmovideooutputoptimizations_setoperationmode.htm
old-project: DirectShow
ms.assetid: 07dc29aa-d3ee-409e-9fe8-0c54d2d6f759
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IDMOVideoOutputOptimizations interface [DirectShow],SetOperationMode method, IDMOVideoOutputOptimizations.SetOperationMode, IDMOVideoOutputOptimizations::SetOperationMode, IDMOVideoOutputOptimizationsSetOperationMode, SetOperationMode, SetOperationMode method [DirectShow], SetOperationMode method [DirectShow],IDMOVideoOutputOptimizations interface, dshow.idmovideooutputoptimizations_setoperationmode, mediaobj/IDMOVideoOutputOptimizations::SetOperationMode
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dmoguids.lib
-	Dmoguids.dll
api_name:
-	IDMOVideoOutputOptimizations.SetOperationMode
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDMOVideoOutputOptimizations::SetOperationMode


## -description



The <code>SetOperationMode</code> method notifies the DMO of the optimization features that are in effect.




## -parameters




### -param ulOutputStreamIndex

Zero-based index of an output stream on the DMO.


### -param dwEnabledFeatures

Bitwise combination of zero or more flags from the <a href="https://msdn.microsoft.com/fafacdd8-d918-491a-a7e5-7b59128f574f">DMO_VIDEO_OUTPUT_STREAM_FLAGS</a> enumeration.


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



Before calling this method, call the <a href="https://msdn.microsoft.com/55916330-8395-4952-a349-f1ab5a3a2d64">IDMOVideoOutputOptimizations::QueryOperationModePreferences</a> method to determine which features the DMO requests. Then call this method to inform the DMO which of those features you are providing. If you are not providing any of them, it is not necessary to call this method. The DMO does not assume that any of them will be provided.

The application must provide all the features it has agreed to. For some features, however, the DMO might not require the feature on every sample. To determine if the DMO can dispense with any features on the next sample, call the <a href="https://msdn.microsoft.com/95acde54-2bdb-4a80-b078-d98945604c7e">IDMOVideoOutputOptimizations::GetCurrentSampleRequirements</a> method. In effect, this enables the DMO to waive an agreed-upon feature for one sample.

Before streaming begins, subsequent calls to this method override earlier calls. To set multiple features, you must do so in a single method call. Once streaming begins, this method returns an error. Streaming begins when the applications calls <a href="https://msdn.microsoft.com/f52e9586-f65d-418f-8c1a-c97c0a81d253">IMediaObject::ProcessInput</a> on at least one input stream.

When streaming ends, the application can renegotiate the features. Streaming ends if the application calls the <a href="https://msdn.microsoft.com/c80001b8-5648-430a-b565-e90486c48ac5">IMediaObject::Flush</a> method, or if the application calls <a href="https://msdn.microsoft.com/1a8e51e2-5d19-423d-acd2-8f1c0a143cf3">IMediaObject::Discontinuity</a> on all the input streams and then processes all of the remaining output.




## -see-also




<a href="https://msdn.microsoft.com/1e87d0e1-68be-4f86-aae2-cff3edfa573b">IDMOVideoOutputOptimizations Interface</a>
 

 

