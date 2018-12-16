---
UID: NN:wmsdkidl.IWMWriterAdvanced
title: IWMWriterAdvanced
author: windows-sdk-content
description: The IWMWriterAdvanced interface provides advanced writing functionality.This interface exists for every instance of the writer object. To obtain a pointer to this interface, call QueryInterface on the writer object.
old-location: wmformat\iwmwriteradvanced.htm
tech.root: wmformat
ms.assetid: 082cd277-157d-42a4-bf37-e47d16f90c7a
ms.author: windowssdkdev
ms.date: 12/5/2018
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
---

# IWMWriterAdvanced interface


## -description



The <b>IWMWriterAdvanced</b> interface provides advanced writing functionality.

This interface exists for every instance of the writer object. To obtain a pointer to this interface, call <b>QueryInterface</b> on the writer object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterAdvanced</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMWriterAdvanced</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd798727(v=VS.85).aspx">AddSink</a>
</td>
<td align="left" width="63%">
Adds a writer sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798728(v=VS.85).aspx">GetSink</a>
</td>
<td align="left" width="63%">
Retrieves a writer sink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798729(v=VS.85).aspx">GetSinkCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of writer sinks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798730(v=VS.85).aspx">GetStatistics</a>
</td>
<td align="left" width="63%">
Retrieves statistics about the current writing operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798731(v=VS.85).aspx">GetSyncTolerance</a>
</td>
<td align="left" width="63%">
Retrieves the amount of time during which the inputs can fall out of synchronization before the samples are discarded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798732(v=VS.85).aspx">GetWriterTime</a>
</td>
<td align="left" width="63%">
Retrieves the clock time that the writer is working to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798734(v=VS.85).aspx">IsRealTime</a>
</td>
<td align="left" width="63%">
Ascertains whether the writer is running in real time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798736(v=VS.85).aspx">RemoveSink</a>
</td>
<td align="left" width="63%">
Removes a writer sink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798737(v=VS.85).aspx">SetLiveSource</a>
</td>
<td align="left" width="63%">
Specifies whether the source is live.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798739(v=VS.85).aspx">SetSyncTolerance</a>
</td>
<td align="left" width="63%">
Sets the amount of time that the inputs can fall out of synchronization before the samples are discarded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798741(v=VS.85).aspx">WriteStreamSample</a>
</td>
<td align="left" width="63%">
Writes a stream sample directly into an ASF file, bypassing the normal compression procedures.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798719(v=VS.85).aspx">IWMWriter Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798721(v=VS.85).aspx">IWMWriterAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>



<a href="https://msdn.microsoft.com/d722b676-bf65-4f91-8118-bb12d3bbb6cb">Writing ASF Files</a>
 

 

