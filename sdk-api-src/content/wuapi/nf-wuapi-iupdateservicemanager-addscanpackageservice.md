---
UID: NF:wuapi.IUpdateServiceManager.AddScanPackageService
title: IUpdateServiceManager::AddScanPackageService
author: windows-sdk-content
description: Registers a scan package as a service with Windows Update Agent (WUA) and then returns an IUpdateService interface.
old-location: wua\iupdateservicemanager_addscanpackageservice.htm
tech.root: wua_sdk
ms.assetid: 5b0677bb-9f19-4bb4-9942-8ca3da18b29a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddScanPackageService, AddScanPackageService method [Windows Update Agent], AddScanPackageService method [Windows Update Agent],IUpdateServiceManager interface, IUpdateServiceManager interface [Windows Update Agent],AddScanPackageService method, IUpdateServiceManager.AddScanPackageService, IUpdateServiceManager::AddScanPackageService, wua.iupdateservicemanager_addscanpackageservice, wuapi/IUpdateServiceManager::AddScanPackageService
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateServiceManager.AddScanPackageService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateServiceManager::AddScanPackageService


## -description


Registers a scan package as a service with Windows Update Agent (WUA) and then returns an <a href="https://msdn.microsoft.com/2f237cd3-668b-4b1b-b98b-4cfc40f5889e">IUpdateService</a> interface.


## -parameters




### -param serviceName [in]

A descriptive name for the scan package service.


### -param scanFileLocation [in]

The path of the Microsoft signed scan file that has to be registered as a service.


### -param flags [in]

Determines how to remove the service registration of the scan package. 

For possible values, see <a href="https://msdn.microsoft.com/c03ee4e7-b8d4-46bb-bc57-20b35d779e07">UpdateServiceOption</a>.


### -param ppService [out]

A pointer to an <a href="https://msdn.microsoft.com/2f237cd3-668b-4b1b-b98b-4cfc40f5889e">IUpdateService</a> interface that contains service registration information.


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

The service that is returned by <b>AddScanPackageService</b> is in the collection of services that the <a href="https://msdn.microsoft.com/9810e56b-a884-454b-adc8-ad839269dae3">Services</a> property of the IUpdateServiceManager interface returns. This service has the special <a href="https://msdn.microsoft.com/1fbd0bb7-23f9-4030-a61e-a85ddc177744">IsScanPackageService</a> property.

An error is returned by <a href="https://msdn.microsoft.com/b7efac6a-ac9f-477a-aada-63fe32208e6f">WinVerifyTrust</a> if the Authorization Cab is not  signed.

This method returns <b>WU_E_INVALID_OPERATION</b> if the object that implements the interface has been locked down.




## -see-also




<a href="https://msdn.microsoft.com/99b451b8-9831-475c-a4b0-7809f78d91b8">IUpdateServiceManager</a>
 

 

