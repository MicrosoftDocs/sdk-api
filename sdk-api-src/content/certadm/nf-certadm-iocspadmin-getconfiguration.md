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

# IOCSPAdmin::GetConfiguration


## -description


The <b>GetConfiguration</b> method connects to an Online Certificate Status Protocol (OCSP) responder server and initializes an <b>OCSPAdmin</b> object with the configuration information from the server.


## -parameters




### -param bstrServerName [in]

A string that contains the responder-server name.


### -param bForce [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td>
<b>VARIANT_TRUE</b> if the caller wants to read the responder configuration from the server's registry when a running instance of the OCSP responder service cannot be found; otherwise, <b>VARIANT_FALSE</b>.

</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td>
<b>True</b> if the caller wants to read the responder configuration from the server's registry when a running instance of the OCSP responder service cannot be found; otherwise, <b>False</b>.

</td>
</tr>
</table>

## -returns



<h3>VB</h3>
 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

If the method returns <b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b>, the configuration is already initialized.

If the method returns <b>E_INVALIDARG</b>, the <i>pVal</i> parameter was set to <b>NULL</b>.




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
 

This method attempts to read the configuration from a running instance of an OCSP responder service, but that might not be possible if the service is not running or is in an inaccessible state. The caller can instruct the method to read the configuration from the server's registry if a running instance cannot be found.

The method fails if you try to call it more than once for a given <b>OCSPAdmin</b> object. Each instance of <b>OCSPAdmin</b> corresponds to one responder server. To connect to another server in an array of OCSP responder servers, create a new instance of an <b>OCSPAdmin</b> object.




## -see-also




<a href="https://msdn.microsoft.com/cf76e934-07a2-46de-b2cf-7f6d3e274d71">IOCSPAdmin</a>
 

 

