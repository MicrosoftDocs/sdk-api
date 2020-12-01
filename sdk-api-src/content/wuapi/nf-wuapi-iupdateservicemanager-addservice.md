---
UID: NF:wuapi.IUpdateServiceManager.AddService
title: IUpdateServiceManager::AddService (wuapi.h)
description: Registers a service with Windows Update Agent (WUA).
helpviewer_keywords: ["AddService","AddService method [Windows Update Agent]","AddService method [Windows Update Agent]","IUpdateServiceManager interface","IUpdateServiceManager interface [Windows Update Agent]","AddService method","IUpdateServiceManager.AddService","IUpdateServiceManager::AddService","wua.iupdateservicemanager_addservice","wuapi/IUpdateServiceManager::AddService"]
old-location: wua\iupdateservicemanager_addservice.htm
tech.root: wua
ms.assetid: b4071ef7-316f-4624-bc43-79c5982c4a82
ms.date: 12/05/2018
ms.keywords: AddService, AddService method [Windows Update Agent], AddService method [Windows Update Agent],IUpdateServiceManager interface, IUpdateServiceManager interface [Windows Update Agent],AddService method, IUpdateServiceManager.AddService, IUpdateServiceManager::AddService, wua.iupdateservicemanager_addservice, wuapi/IUpdateServiceManager::AddService
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
ms.custom: 19H1
f1_keywords:
 - IUpdateServiceManager::AddService
 - wuapi/IUpdateServiceManager::AddService
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
 - IUpdateServiceManager.AddService
---

# IUpdateServiceManager::AddService


## -description

Registers a service with Windows Update Agent (WUA).

## -parameters

### -param serviceID [in]

An identifier for a service to be registered.

### -param authorizationCabPath [in]

The path of the Microsoft signed local cabinet file that has the information that is required for a service registration.

### -param retval [out]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservice">IUpdateService</a> interface that represents an added service.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

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
<dt><b>WU_E_DS_SERVICEEXPIRED</b></dt>
</dl>
</td>
<td width="60%">
The Authorization Cab has expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_DS_INVALIDOPERATION</b></dt>
</dl>
</td>
<td width="60%">
The state of Automatic Updates could not be changed.

</td>
</tr>
</table>

## -remarks

This method returns <b>WU_E_DS_INVALIDOPERATION</b> if the requested change in the state of Automatic Updates is contrary to the specifications in the Authorization Cab. An error is returned by <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> if the Authorization Cab has not been signed.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager">IUpdateServiceManager</a>