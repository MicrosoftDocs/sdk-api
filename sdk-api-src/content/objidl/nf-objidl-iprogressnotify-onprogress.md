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

# IProgressNotify::OnProgress


## -description


Notifies registered objects and applications of the progress of a downloading operation.


## -parameters




### -param dwProgressCurrent [in]

The amount of data available.


### -param dwProgressMaximum [in]

The total amount of data to be downloaded.


### -param fAccurate [in]

Indicates the accuracy of the values in <i>dwProgressCurrent</i> and <i>dwProgressMaximum</i>. They are either reliable (<b>TRUE</b>) or unreliable (<b>FALSE</b>). The <b>FALSE</b> value indicates that control structures for determining the actual position of, or amount of, data yet to be downloaded are not available.


### -param fOwner [in]

Indicates whether this <b>OnProgress</b> call can control the blocking behavior of the operation. If <b>TRUE</b>, the caller can use return values from <b>OnProgress</b> to block (STG_S_BLOCK), retry (STG_S_RETRYNOW), or monitor (STG_S_MONITORING) the operation. If <b>FALSE</b>, the return value from <b>OnProgress</b> has no influence on blocking behavior.


## -returns



This method can return the standard return values E_FAIL, E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_S_RETRYNOW</b></dt>
</dl>
</td>
<td width="60%">
The caller is to retry the operation immediately. (This value is most useful for applications that do blocking from within the callback routine.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_S_BLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller is to block the download and retry the call as needed to determine if additional data is available. This is the default behavior if no sinks are registered on the connection point.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_S_MONITORING</b></dt>
</dl>
</td>
<td width="60%">
The callback recipient reliquishes control of the downloading process to one of the other objects or applications that have registered progress notification sinks on the same stream. This is useful if the notification sink is interested only in gathering statistics.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Data is currently unavailable. The caller is to try again after some desired interval. The notification sink returns this value if the asynchronous storage is to operate in nonblocking mode.


</td>
</tr>
</table>
 




## -remarks



Sinks may be inherited by any substorage or substream of a given storage. If no sink is registered, the thread will block until the requested data becomes available, or the download is canceled by the downloader.

Where multiple objects or applications have registered progress notification sinks on a single stream, only one of them can control the behavior of a download. Ownership of the download goes to the first sink to register with the storage or stream, or any advise skinks that may have been inherited from the parent storage (if the storage was created with ASYNC_MODE_COMPATIBILITY.) 

Any one of the sinks can relinquish control to the next connection point by returning STG_S_MONITORING to the connection point making the current caller. After a connection point obtains control (through receiving STG_S_BLOCK or STG_S_RETRYNOW), all subsequent connection points calling <b>OnProgress</b> will set <i>fOwner</i> to <b>FALSE</b>.





## -see-also




<a href="https://msdn.microsoft.com/3f90437d-df8f-42b2-af81-519bfb9577b1">IProgressNotify</a>
 

 

