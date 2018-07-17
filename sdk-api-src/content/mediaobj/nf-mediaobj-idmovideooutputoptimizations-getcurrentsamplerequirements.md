---
UID: NF:mediaobj.IDMOVideoOutputOptimizations.GetCurrentSampleRequirements
title: IDMOVideoOutputOptimizations::GetCurrentSampleRequirements
author: windows-sdk-content
description: The GetCurrentSampleRequirements method retrieves the optimization features required to process the next sample, given the features already agreed to by the application.
old-location: dshow\idmovideooutputoptimizations_getcurrentsamplerequirements.htm
old-project: DirectShow
ms.assetid: 95acde54-2bdb-4a80-b078-d98945604c7e
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetCurrentSampleRequirements, GetCurrentSampleRequirements method [DirectShow], GetCurrentSampleRequirements method [DirectShow],IDMOVideoOutputOptimizations interface, IDMOVideoOutputOptimizations interface [DirectShow],GetCurrentSampleRequirements method, IDMOVideoOutputOptimizations.GetCurrentSampleRequirements, IDMOVideoOutputOptimizations::GetCurrentSampleRequirements, IDMOVideoOutputOptimizationsGetCurrentSampleRequirements, dshow.idmovideooutputoptimizations_getcurrentsamplerequirements, mediaobj/IDMOVideoOutputOptimizations::GetCurrentSampleRequirements
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDMOVideoOutputOptimizations::GetCurrentSampleRequirements


## -description



The <code>GetCurrentSampleRequirements</code> method retrieves the optimization features required to process the next sample, given the features already agreed to by the application.




## -parameters




### -param ulOutputStreamIndex

Zero-based index of an output stream on the DMO.


### -param pdwRequestedFeatures

Pointer to a variable that receives the required features. The returned value is a bitwise combination of zero or more flags from the <a href="https://msdn.microsoft.com/fafacdd8-d918-491a-a7e5-7b59128f574f">DMO_VIDEO_OUTPUT_STREAM_FLAGS</a> enumeration.


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



After an application calls the <a href="https://msdn.microsoft.com/07dc29aa-d3ee-409e-9fe8-0c54d2d6f759">IDMOVideoOutputOptimizations::SetOperationMode</a> method, it must provide all the features it has agreed to. However, the DMO might not require every feature on every sample. This method enables the DMO to waive an agreed-upon feature for one sample.

Before processing a sample, the application can call this method. If the DMO does not require a given feature in order to process the next sample, it omits the corresponding flag from the <i>pdwRequestedFeatures</i> parameter. For the next sample only, the application can ignore the feature. The results of this method are valid only for the next call to the <a href="https://msdn.microsoft.com/1a3b1192-f1e9-4f04-b543-d38692502b8e">IMediaObject::ProcessOutput</a> method.

The DMO will return only the flags that were agreed to in the <b>SetOperationMode</b> method. In other words, you cannot dynamically enable new features with this method.




## -see-also




<a href="https://msdn.microsoft.com/1e87d0e1-68be-4f86-aae2-cff3edfa573b">IDMOVideoOutputOptimizations Interface</a>
 

 

