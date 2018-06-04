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

# IUpdateServiceManager::AddScanPackageService


## -description


Registers a scan package as a service with Windows Update Agent (WUA) and then returns an <a href="https://msdn.microsoft.com/2f237cd3-668b-4b1b-b98b-4cfc40f5889e">IUpdateService</a> interface.


## -parameters




### -param serviceName




### -param scanFileLocation




### -param flags [in]

Determines how to remove the service registration of the scan package. 

For possible values, see <a href="https://msdn.microsoft.com/c03ee4e7-b8d4-46bb-bc57-20b35d779e07">UpdateServiceOption</a>.


### -param ppService [out]

A pointer to an <a href="https://msdn.microsoft.com/2f237cd3-668b-4b1b-b98b-4cfc40f5889e">IUpdateService</a> interface that contains service registration information.


#### - bstrScanFileLocation [in]

The path of the Microsoft signed scan file that has to be registered as a service.


#### - bstrServiceName [in]

A descriptive name for the scan package service.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. This method can also return the following error codes.

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
<dt><b>WU_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The computer could not access the update site.

</td>
</tr>
</table>
 




## -remarks



You can use the ID of the service in searches by passing the ID as the <a href="https://msdn.microsoft.com/7c00d26a-9ef0-45ec-81b3-d13f91dd7d8d">ServiceID</a> property of the <a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a> interface.

To free resources, remove the service after it is no longer needed. Use the  <a href="https://msdn.microsoft.com/fedd0979-1cc1-40c7-93d1-ade2f069ee76">RemoveService</a> method to remove the service.

Do not  call the <a href="https://msdn.microsoft.com/ea54d96a-9ffb-4abd-a032-4dfcc7ba6403">RegisterServiceWithAU</a> method for the service that  the <b>AddScanPackageService</b> method registers.

The service that is returned by <b>AddScanPackageService</b> is in the collection of services that the <a href="https://msdn.microsoft.com/library/windows/hardware/dn926947">Services</a> property of the IUpdateServiceManager interface returns. This service has the special <a href="https://msdn.microsoft.com/1fbd0bb7-23f9-4030-a61e-a85ddc177744">IsScanPackageService</a> property.

An error is returned by <a href="https://msdn.microsoft.com/b7efac6a-ac9f-477a-aada-63fe32208e6f">WinVerifyTrust</a> if the Authorization Cab is not  signed.

This method returns <b>WU_E_INVALID_OPERATION</b> if the object that implements the interface has been locked down.




## -see-also




<a href="https://msdn.microsoft.com/99b451b8-9831-475c-a4b0-7809f78d91b8">IUpdateServiceManager</a>
 

 

