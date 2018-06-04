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

# IOCSPAdmin::SetConfiguration


## -description


The <b>SetConfiguration</b> method updates a responder service  with configuration changes.


## -parameters




### -param bstrServerName [in]

A string that contains the responder-service name.


### -param bForce [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td><b>VARIANT_TRUE</b> if the method should update the responder service registry when the service is offline or unavailable; otherwise, <b>VARIANT_FALSE</b>. If the service is offline or unavailable and the <i>bForce</i> parameter is <b>VARIANT_TRUE</b>, <b>SetConfiguration</b> updates the responder service registry directly.

</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td><b>True</b> if the method should update the responder service registry when the service is offline or unavailable; otherwise, <b>False</b>. If the service is offline or unavailable and the <i>bForce</i> parameter is <b>True</b>, <b>SetConfiguration</b> updates the responder service registry directly.

</td>
</tr>
</table>

## -returns



<h3>VB</h3>
 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The following table lists the effects of the <i>bForce</i> parameter value on the method call.

<table>
<tr>
<th>OCSP responder service on the target server</th>
<th><i>bForce</i> is <b>VARIANT_TRUE</b></th>
<th><i>bForce</i> is <b>VARIANT_FALSE</b></th>
</tr>
<tr>
<td>
Running

</td>
<td>
Retrieve configuration from the service.

</td>
<td>
Retrieve configuration from the service.

</td>
</tr>
<tr>
<td>
Stopped

</td>
<td>
Attempt to retrieve configuration from the server registry. If this attempt fails, return an error.

</td>
<td>
Return an error.

</td>
</tr>
</table>
 

The following table lists the effects of the <i>bForce</i> parameter value on the method call.

<table>
<tr>
<th>OCSP responder service on the target server</th>
<th><i>bForce</i> is <b>True</b></th>
<th><i>bForce</i> is <b>False</b></th>
</tr>
<tr>
<td>
Running

</td>
<td>
Retrieve configuration from the service.

</td>
<td>
Retrieve configuration from the service.

</td>
</tr>
<tr>
<td>
Stopped

</td>
<td>
Attempt to retrieve configuration from the server registry. If this attempt fails, return an error.

</td>
<td>
Return an error.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cf76e934-07a2-46de-b2cf-7f6d3e274d71">IOCSPAdmin</a>
 

 

