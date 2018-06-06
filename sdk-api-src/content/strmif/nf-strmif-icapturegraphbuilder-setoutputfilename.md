---
UID: NF:strmif.ICaptureGraphBuilder.SetOutputFileName
title: ICaptureGraphBuilder::SetOutputFileName
author: windows-sdk-content
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Creates the rendering section of the filter graph, which will save bits to disk with the specified file name.
old-location: dshow\icapturegraphbuilder_setoutputfilename.htm
old-project: DirectShow
ms.assetid: f410465f-c560-49ab-9194-66d708274f77
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ICaptureGraphBuilder interface [DirectShow],SetOutputFileName method, ICaptureGraphBuilder.SetOutputFileName, ICaptureGraphBuilder::SetOutputFileName, ICaptureGraphBuilderSetOutputFileName, SetOutputFileName, SetOutputFileName method [DirectShow], SetOutputFileName method [DirectShow],ICaptureGraphBuilder interface, dshow.icapturegraphbuilder_setoutputfilename, strmif/ICaptureGraphBuilder::SetOutputFileName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Reference:\_Dshowh
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Quartz.dll
api_name:
 - ICaptureGraphBuilder.SetOutputFileName
product: Windows
targetos: Windows
req.lib: 
req.dll: Quartz.dll
req.irql: 
req.product: Windows XP with SP1
---

# ICaptureGraphBuilder::SetOutputFileName


## -description



<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/abdf6fb2-e98f-4df8-98ec-06d33798abb5">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Creates the rendering section of the filter graph, which will save bits to disk with the specified file name.




## -parameters




### -param pType [in]

Pointer to a <b>GUID</b> representing the media subtype. Must be <code>&amp;MEDIASUBTYPE_Avi</code>.


### -param lpstrFile




### -param ppf [out]

Address of a pointer to an <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface representing the multiplexer filter. This method increments the reference count on the <b>IBaseFilter</b> interface so you must decrement the reference count by using the <b>Release</b> method on this parameter when done using the filter.


### -param ppSink






#### - lpwstrFile [in]

Pointer to a wide-character string containing the output file name.


#### - pSink [out]

Address of a pointer to an <a href="https://msdn.microsoft.com/aa1d3f8e-9790-4442-ba7e-896981bf1b96">IFileSinkFilter</a> interface representing the file writer. This method increments the reference count on the IFileSinkFilter interface so you must decrement the reference count using <b>Release</b> when done using the filter.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. Audio-Video Interleaved (AVI) is the only supported output format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NOERROR</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Instance of the AVI multiplexer filter was successfully created.

</td>
</tr>
</table>
 




## -remarks



This method inserts the multiplexer and the file writer into the filter graph and calls <a href="https://msdn.microsoft.com/d202be46-0a7a-4097-adf6-6ec9c6274449">IFileSinkFilter::SetFileName</a> to set the output file name.

You can use the <i>ppf</i> parameter returned by this method as the <i>pfRenderer</i> parameter in calls to <a href="https://msdn.microsoft.com/2b174f31-d7bb-4934-9d5b-2e4fd6ae8bf5">RenderStream</a>.

You can use the <i>pSink</i> parameter from this method in a call to <a href="https://msdn.microsoft.com/d202be46-0a7a-4097-adf6-6ec9c6274449">SetFileName</a> to change the file name set by <code>ICaptureGraphBuilder::SetOutputFileName</code>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/64ee80cd-9f63-4f38-853a-1ecfc03e6076">ICaptureGraphBuilder Interface</a>
 

 

