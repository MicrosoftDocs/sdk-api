---
UID: NF:wuapi.IUpdateServiceManager.AddService
title: IUpdateServiceManager::AddService (wuapi.h)
author: windows-sdk-content
description: Registers a service with Windows Update Agent (WUA).
old-location: wua\iupdateservicemanager_addservice.htm
tech.root: Wua_Sdk
ms.assetid: b4071ef7-316f-4624-bc43-79c5982c4a82
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddService, AddService method [Windows Update Agent], AddService method [Windows Update Agent],IUpdateServiceManager interface, IUpdateServiceManager interface [Windows Update Agent],AddService method, IUpdateServiceManager.AddService, IUpdateServiceManager::AddService, wua.iupdateservicemanager_addservice, wuapi/IUpdateServiceManager::AddService
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
 - IUpdateServiceManager.AddService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

An <a href="https://msdn.microsoft.com/2f237cd3-668b-4b1b-b98b-4cfc40f5889e">IUpdateService</a> interface that represents an added service.


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



This method returns <b>WU_E_DS_INVALIDOPERATION</b> if the requested change in the state of Automatic Updates is contrary to the specifications in the Authorization Cab. An error is returned by <a href="https://msdn.microsoft.com/b7efac6a-ac9f-477a-aada-63fe32208e6f">WinVerifyTrust</a> if the Authorization Cab has not been signed.




## -see-also




<a href="https://msdn.microsoft.com/99b451b8-9831-475c-a4b0-7809f78d91b8">IUpdateServiceManager</a>
 

 

