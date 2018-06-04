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

# ConvertPerformanceCounterToAuxiliaryCounter function


## -description


Converts the specified performance counter value to the corresponding auxiliary counter value; optionally provides the estimated conversion error in nanoseconds due to latencies and maximum possible drift. 


## -parameters




### -param ullPerformanceCounterValue [in]

The performance counter value to convert.


### -param lpAuxiliaryCounterValue [out]

On success, contains the converted auxiliary counter value. Will be undefined if the function fails.


### -param lpConversionError [out, optional]

On success, contains the estimated conversion error, in nanoseconds. Will be undefined if the function fails.


## -returns



Returns <b>S_OK</b> if the conversion succeeds; otherwise, returns another <b>HRESULT</b> specifying the error. 

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The auxiliary counter is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The value to convert is outside the permitted range (+/- 10 seconds from when the called occurred).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The value to convert is prior to the last system boot or S3/S4 transition.

</td>
</tr>
</table>
 



