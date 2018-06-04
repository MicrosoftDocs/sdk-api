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

# IComApp2Events::OnAppRecycle2


## -description


Generated when the server application process is marked for recycling termination.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidApp [in]

The application ID.


### -param guidProcess [in]

The process ID.


### -param lReason [in]

The reason code that explains why a process was recycled. The following codes are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRR_NO_REASON_SUPPLIED"></a><a id="crr_no_reason_supplied"></a><dl>
<dt><b>CRR_NO_REASON_SUPPLIED</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The reason is not specified.

</td>
</tr>
<tr>
<td width="40%"><a id="CRR_LIFETIME_LIMIT"></a><a id="crr_lifetime_limit"></a><dl>
<dt><b>CRR_LIFETIME_LIMIT</b></dt>
<dt>xFFFFFFFF</dt>
</dl>
</td>
<td width="60%">
The specified number of minutes that an application runs before recycling was reached.

</td>
</tr>
<tr>
<td width="40%"><a id="CRR_ACTIVATION_LIMIT"></a><a id="crr_activation_limit"></a><dl>
<dt><b>CRR_ACTIVATION_LIMIT</b></dt>
<dt>0xFFFFFFFE</dt>
</dl>
</td>
<td width="60%">
The specified number of activations was reached.

</td>
</tr>
<tr>
<td width="40%"><a id="CRR_CALL_LIMIT"></a><a id="crr_call_limit"></a><dl>
<dt><b>CRR_CALL_LIMIT</b></dt>
<dt>0xFFFFFFFD</dt>
</dl>
</td>
<td width="60%">
The specified number of calls to configured objects in the application was reached.

</td>
</tr>
<tr>
<td width="40%"><a id="CRR_MEMORY_LIMIT"></a><a id="crr_memory_limit"></a><dl>
<dt><b>CRR_MEMORY_LIMIT</b></dt>
<dt>0xFFFFFFFC</dt>
</dl>
</td>
<td width="60%">
The specified memory usage that a process cannot exceed was reached.

</td>
</tr>
<tr>
<td width="40%"><a id="CRR_RECYCLED_FROM_UI"></a><a id="crr_recycled_from_ui"></a><dl>
<dt><b>CRR_RECYCLED_FROM_UI</b></dt>
<dt>xFFFFFFFB</dt>
</dl>
</td>
<td width="60%">
An administrator decided to recycle the process through the Component Services administration tool.

</td>
</tr>
</table>
 


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/45e0d26b-7485-436b-9b64-fa48217b32d1">IComApp2Events</a>
 

 

