---
UID: NN:wmsdkidl.IWMWriterAdvanced
title: IWMWriterAdvanced (wmsdkidl.h)
author: windows-sdk-content
description: The IWMWriterAdvanced interface provides advanced writing functionality.This interface exists for every instance of the writer object. To obtain a pointer to this interface, call QueryInterface on the writer object.
old-location: wmformat\iwmwriteradvanced.htm
tech.root: wmformat
ms.assetid: 082cd277-157d-42a4-bf37-e47d16f90c7a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMWriterAdvanced, IWMWriterAdvanced interface [windows Media Format], IWMWriterAdvanced interface [windows Media Format],described, IWMWriterAdvancedInterface, wmformat.iwmwriteradvanced, wmsdkidl/IWMWriterAdvanced
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMWriterAdvanced
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterAdvanced interface


## -description



The <b>IWMWriterAdvanced</b> interface provides advanced writing functionality.

This interface exists for every instance of the writer object. To obtain a pointer to this interface, call <b>QueryInterface</b> on the writer object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterAdvanced</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMWriterAdvanced</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterAdvanced</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink">AddSink</a>
</td>
<td align="left" width="63%">
Adds a writer sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink">GetSink</a>
</td>
<td align="left" width="63%">
Retrieves a writer sink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount">GetSinkCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of writer sinks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics">GetStatistics</a>
</td>
<td align="left" width="63%">
Retrieves statistics about the current writing operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsynctolerance">GetSyncTolerance</a>
</td>
<td align="left" width="63%">
Retrieves the amount of time during which the inputs can fall out of synchronization before the samples are discarded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getwritertime">GetWriterTime</a>
</td>
<td align="left" width="63%">
Retrieves the clock time that the writer is working to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-isrealtime">IsRealTime</a>
</td>
<td align="left" width="63%">
Ascertains whether the writer is running in real time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink">RemoveSink</a>
</td>
<td align="left" width="63%">
Removes a writer sink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setlivesource">SetLiveSource</a>
</td>
<td align="left" width="63%">
Specifies whether the source is live.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance">SetSyncTolerance</a>
</td>
<td align="left" width="63%">
Sets the amount of time that the inputs can fall out of synchronization before the samples are discarded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample">WriteStreamSample</a>
</td>
<td align="left" width="63%">
Writes a stream sample directly into an ASF file, bypassing the normal compression procedures.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2">IWMWriterAdvanced2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writing-asf-files">Writing ASF Files</a>
 

 

