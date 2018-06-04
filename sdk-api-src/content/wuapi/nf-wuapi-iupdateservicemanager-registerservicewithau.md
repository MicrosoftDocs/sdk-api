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

# IUpdateServiceManager::RegisterServiceWithAU


## -description


Registers a service with Automatic Updates.


## -parameters




### -param serviceID [in]

An identifier for the service to be registered.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns  a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
A parameter value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This method cannot be called from a remote computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_DS_UNKNOWNSERVICE</b></dt>
</dl>
</td>
<td width="60%">
An attempt to register an unknown service. 


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_DS_NEEDWINDOWSSERVICE</b></dt>
</dl>
</td>
<td width="60%">
The Windows Update service  could not be removed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The computer could not access the update site, or the state of Automatic Updates could not be changed.

</td>
</tr>
</table>
 




## -remarks



This method returns <b>WU_E_DS_UNKNOWNSERVICE</b> if the service to be registered is unknown to Automatic Updates.

This method returns <b>WU_E_INVALID_OPERATION</b> if the method is called with an invalid service ID.  This method also returns <b>WU_E_INVALID_OPERATION</b> if the service ID is valid but the service can't register with Automatic Updates. That is,  the requested change in the state of Automatic Updates is contrary to the specifications in the authorization cabinet file (for example, <a href="https://msdn.microsoft.com/79198de8-548a-4d9a-ae07-d421babe8700">CanRegisterWithAU</a> property is set to <b>FALSE</b>). An error is returned by <a href="https://msdn.microsoft.com/b7efac6a-ac9f-477a-aada-63fe32208e6f">WinVerifyTrust</a> function if the authorization cabinet file has not been signed.



This method returns <b>WU_E_DS_NEEDWINDOWSSERVICE</b> if you try to remove the Windows Update service.




## -see-also




<a href="https://msdn.microsoft.com/99b451b8-9831-475c-a4b0-7809f78d91b8">IUpdateServiceManager</a>
 

 

