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

# IAudioProcessingObjectConfiguration::LockForProcess


## -description


The <code>LockForProcess</code> method is used to verify that the APO is locked and ready to process data.


## -parameters




### -param u32NumInputConnections [in]

Number of input connections that are attached to this APO.


### -param ppInputConnections [in]

Connection descriptor for each input connection that is attached to this APO.


### -param u32NumOutputConnections [in]

Number of output connections that are attached to this APO.


### -param ppOutputConnections [in]

Connection descriptor for each output connection that is attached to this APO.


## -returns



The <code>LockForProcess</code> method returns a value of S_OK if the call is completed successfully. At this stage, the APO is locked and is ready to process data.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer was passed to function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APOERR_INVALID_CONNECITON_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
Invalid connection format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APOERR_NUM_CONNECTIONS_INVALID</b></dt>
</dl>
</td>
<td width="60%">
Number of input or output connections not valid on this APO.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APOERR_APO_LOCKED</b></dt>
</dl>
</td>
<td width="60%">
APO is already locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other HRESULTS</b></dt>
</dl>
</td>
<td width="60%">
These failures will be tracked by the audio engine.

</td>
</tr>
</table>
 




## -remarks



When the <code>LockForProcess</code> method is called, it first performs an internal check to see if the APO has been initialized and is ready to process data. Each APO has different initialization requirements so each APO must define its own Initialize method if needed.



