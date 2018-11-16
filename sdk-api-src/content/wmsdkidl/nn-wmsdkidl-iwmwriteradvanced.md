---
UID: NN:wmsdkidl.IWMWriterAdvanced
title: IWMWriterAdvanced
author: windows-sdk-content
description: The IWMWriterAdvanced interface provides advanced writing functionality.This interface exists for every instance of the writer object. To obtain a pointer to this interface, call QueryInterface on the writer object.
old-location: wmformat\iwmwriteradvanced.htm
tech.root: wmformat
ms.assetid: 082cd277-157d-42a4-bf37-e47d16f90c7a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMWriterAdvanced, IWMWriterAdvanced interface [windows Media Format], IWMWriterAdvanced interface [windows Media Format],described, IWMWriterAdvancedInterface, wmformat.iwmwriteradvanced, wmsdkidl/IWMWriterAdvanced
ms.prod: windows-hardware
ms.technology: windows-devices
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
<a href="https://msdn.microsoft.com/65763ac3-fba0-4de6-9c2e-4e241bbe5f13">AddSink</a>
</td>
<td align="left" width="63%">
Adds a writer sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6775eb89-a3af-42d2-b1e3-197abb1fce61">GetSink</a>
</td>
<td align="left" width="63%">
Retrieves a writer sink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/210c96bc-3659-43e6-acb2-4d9f328e81e0">GetSinkCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of writer sinks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/005c2039-e821-42ab-bead-1bf40f2ab171">GetStatistics</a>
</td>
<td align="left" width="63%">
Retrieves statistics about the current writing operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f62d3405-3125-4df6-bd06-fa70358560ad">GetSyncTolerance</a>
</td>
<td align="left" width="63%">
Retrieves the amount of time during which the inputs can fall out of synchronization before the samples are discarded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed15e545-8b37-4098-8e2f-96f4cfb271d3">GetWriterTime</a>
</td>
<td align="left" width="63%">
Retrieves the clock time that the writer is working to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d00eb78-d90e-41a0-9bba-305ac65057f3">IsRealTime</a>
</td>
<td align="left" width="63%">
Ascertains whether the writer is running in real time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2fc7f82-981a-4f69-b99d-71514ed2c6ae">RemoveSink</a>
</td>
<td align="left" width="63%">
Removes a writer sink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab015f92-498e-44c7-95c9-869dfdfccc09">SetLiveSource</a>
</td>
<td align="left" width="63%">
Specifies whether the source is live.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d60020bf-52f1-46a0-aeae-367e3b179fac">SetSyncTolerance</a>
</td>
<td align="left" width="63%">
Sets the amount of time that the inputs can fall out of synchronization before the samples are discarded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/498bfb73-bfa5-429d-ae8a-3a691fc25fc2">WriteStreamSample</a>
</td>
<td align="left" width="63%">
Writes a stream sample directly into an ASF file, bypassing the normal compression procedures.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/a194ef11-5203-4e85-af91-cdce0c53fe76">IWMWriter Interface</a>



<a href="https://msdn.microsoft.com/94790b67-690c-4a0f-9b82-801bfcec9eb0">IWMWriterAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>



<a href="https://msdn.microsoft.com/d722b676-bf65-4f91-8118-bb12d3bbb6cb">Writing ASF Files</a>
 

 

