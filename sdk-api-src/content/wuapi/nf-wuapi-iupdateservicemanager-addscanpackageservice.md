---
UID: NF:wuapi.IUpdateServiceManager.AddScanPackageService
title: IUpdateServiceManager::AddScanPackageService (wuapi.h)
description: Registers a scan package as a service with Windows Update Agent (WUA) and then returns an IUpdateService interface.
helpviewer_keywords: ["AddScanPackageService","AddScanPackageService method [Windows Update Agent]","AddScanPackageService method [Windows Update Agent]","IUpdateServiceManager interface","IUpdateServiceManager interface [Windows Update Agent]","AddScanPackageService method","IUpdateServiceManager.AddScanPackageService","IUpdateServiceManager::AddScanPackageService","wua.iupdateservicemanager_addscanpackageservice","wuapi/IUpdateServiceManager::AddScanPackageService"]
old-location: wua\iupdateservicemanager_addscanpackageservice.htm
tech.root: wua
ms.assetid: 5b0677bb-9f19-4bb4-9942-8ca3da18b29a
ms.date: 12/05/2018
ms.keywords: AddScanPackageService, AddScanPackageService method [Windows Update Agent], AddScanPackageService method [Windows Update Agent],IUpdateServiceManager interface, IUpdateServiceManager interface [Windows Update Agent],AddScanPackageService method, IUpdateServiceManager.AddScanPackageService, IUpdateServiceManager::AddScanPackageService, wua.iupdateservicemanager_addscanpackageservice, wuapi/IUpdateServiceManager::AddScanPackageService
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
ms.custom: 19H1
f1_keywords:
 - IUpdateServiceManager::AddScanPackageService
 - wuapi/IUpdateServiceManager::AddScanPackageService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateServiceManager.AddScanPackageService
---

# IUpdateServiceManager::AddScanPackageService


## -description

Registers a scan package as a service with Windows Update Agent (WUA) and then returns an <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservice">IUpdateService</a> interface.

## -parameters

### -param serviceName [in]

A descriptive name for the scan package service.

### -param scanFileLocation [in]

The path of the Microsoft signed scan file that has to be registered as a service.

### -param flags [in]

Determines how to remove the service registration of the scan package. 

For possible values, see <a href="/windows/desktop/api/wuapi/ne-wuapi-updateserviceoption">UpdateServiceOption</a>.

### -param ppService [out]

A pointer to an <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservice">IUpdateService</a> interface that contains service registration information.

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

You can use the ID of the service in searches by passing the ID as the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_serviceid">ServiceID</a> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface.

To free resources, remove the service after it is no longer needed. Use the  <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-removeservice">RemoveService</a> method to remove the service.

Do not  call the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau">RegisterServiceWithAU</a> method for the service that  the <b>AddScanPackageService</b> method registers.

The service that is returned by <b>AddScanPackageService</b> is in the collection of services that the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-get_services">Services</a> property of the IUpdateServiceManager interface returns. This service has the special <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateservice-get_isscanpackageservice">IsScanPackageService</a> property.

An error is returned by <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> if the Authorization Cab is not  signed.

This method returns <b>WU_E_INVALID_OPERATION</b> if the object that implements the interface has been locked down.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager">IUpdateServiceManager</a>