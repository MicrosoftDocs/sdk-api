---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMFASFMultiplexer::SetSyncTolerance


## -description



Sets the maximum time by which samples from various streams can be out of synchronization. The multiplexer will not accept a sample with a time stamp that is out of synchronization with the latest samples from any other stream by an amount that exceeds the synchronization tolerance.




## -parameters




### -param msSyncTolerance [in]

Synchronization tolerance in milliseconds.


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
</table>
 




## -remarks



The synchronization tolerance is the maximum difference in presentation times at any given point between samples of different streams that the ASF multiplexer can accommodate. That is, if the synchronization tolerance is 3 seconds, no stream can be more than 3 seconds behind any other stream in the time stamps passed to the multiplexer. The multiplexer determines a default synchronization tolerance to use, but this method overrides it (usually to increase it). More tolerance means the potential for greater latency in the multiplexer. If the time stamps are synchronized among the streams, actual latency will be much lower than <i>msSyncTolerance</i>.




## -see-also




<a href="https://msdn.microsoft.com/007a6da5-47cf-476a-b0f7-566a68ad19ce">ASF Multiplexer</a>



<a href="https://msdn.microsoft.com/bdb549b5-425b-4f77-b413-723ceb7acd11">IMFASFMultiplexer</a>
 

 

