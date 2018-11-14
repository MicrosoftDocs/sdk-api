---
UID: NN:sbe.IStreamBufferRecordControl
title: IStreamBufferRecordControl
author: windows-sdk-content
description: The IStreamBufferRecordControl interface is used to control stream buffer Recording objects.Use the IStreamBufferSink::CreateRecorder method on the Stream Buffer Sink filter to create new Recording objects.
old-location: mstv\istreambufferrecordcontrol.htm
tech.root: MSTV
ms.assetid: f196638e-ccbb-4768-96c1-8e1d00361831
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IStreamBufferRecordControl, IStreamBufferRecordControl interface [Microsoft TV Technologies], IStreamBufferRecordControl interface [Microsoft TV Technologies],described, IStreamBufferRecordControlInterface, mstv.istreambufferrecordcontrol, sbe/IStreamBufferRecordControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
 - Sbe.h
api_name:
 - IStreamBufferRecordControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamBufferRecordControl interface


## -description



The <b>IStreamBufferRecordControl</b> interface is used to control stream buffer <a href="https://msdn.microsoft.com/717a3b99-d998-4e64-aab6-6b06e18991da">Recording</a> objects.

Use the <a href="https://msdn.microsoft.com/a9f3b7e1-4f54-4802-af24-4b791ee646fc">IStreamBufferSink::CreateRecorder</a> method on the Stream Buffer Sink filter to create new Recording objects. After making a recording, stop the <b>Recording</b> object and release it before releasing the Stream Buffer Sink filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferRecordControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStreamBufferRecordControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferRecordControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/313f2ad0-7401-4a36-a229-abfc67737324">GetRecordingStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of the <b>Recording</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e72ec34e-d3e3-4f5f-9336-d55135dc1e47">Start</a>
</td>
<td align="left" width="63%">
Starts a recording at a specified time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b6a3ac4-076a-4fca-909c-6063637248a8">Stop</a>
</td>
<td align="left" width="63%">
Ends a recording at a specified time.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferRecordControl)</code>.




## -see-also




<a href="https://msdn.microsoft.com/1aee15a3-5bc8-401b-9b37-b9351fd7c91f">Creating Stream Buffer Recordings</a>



<a href="https://msdn.microsoft.com/b3e8703a-2b69-4262-9aaa-ff9ac8ca2f28">Stream Buffer Engine Interfaces</a>
 

 

