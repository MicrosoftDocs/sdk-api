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

# INetFwServiceRestriction::RestrictService


## -description


The <b>RestrictService</b> method turns service restriction on or off for a given service.


## -parameters




### -param serviceName [in]

Name of the service for which service restriction is being turned on or off.


### -param appName [in]

Name of the application for which service restriction is being turned on or off.


### -param restrictService [in]

Indicates whether service restriction is being turned on or off.  If this value is true (<b>VARIANT_TRUE</b>), the service will be restricted when sending or receiving network traffic.  The Windows Service Hardening rules collection can contain rules which can allow this service specific inbound or outbound network access per specific requirements.  If false (<b>VARIANT_FALSE</b>), the service is not restricted by Windows Service Hardening.


### -param serviceSidRestricted [in]

Indicates the type of service SID for the specified service.  If this value is true (<b>VARIANT_TRUE</b>), the service SID will be restricted.  Otherwise, it will be unrestricted.


## -returns



<h3>C++</h3>

						If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted due to permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid parameter.

</td>
</tr>
</table>
 

<h3>VB</h3>

						If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted due to permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid parameter.

</td>
</tr>
</table>
 




## -remarks



When adding rules, note that there may be a small time lag before the newly-added rule is applied.




## -see-also




<a href="https://msdn.microsoft.com/e426cae9-8c39-44cf-bd48-3b385fdfbdf7">INetFwServiceRestriction</a>
 

 

