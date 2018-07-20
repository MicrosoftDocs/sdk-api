---
UID: NF:wuapi.IUpdateServiceManager.RegisterServiceWithAU
title: IUpdateServiceManager::RegisterServiceWithAU
author: windows-sdk-content
description: Registers a service with Automatic Updates.
old-location: wua\iupdateservicemanager_registerservicewithau.htm
old-project: Wua_Sdk
ms.assetid: ea54d96a-9ffb-4abd-a032-4dfcc7ba6403
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IUpdateServiceManager interface [Windows Update Agent],RegisterServiceWithAU method, IUpdateServiceManager.RegisterServiceWithAU, IUpdateServiceManager::RegisterServiceWithAU, RegisterServiceWithAU, RegisterServiceWithAU method [Windows Update Agent], RegisterServiceWithAU method [Windows Update Agent],IUpdateServiceManager interface, wua.iupdateservicemanager_registerservicewithau, wuapi/IUpdateServiceManager::RegisterServiceWithAU
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateServiceManager.RegisterServiceWithAU
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
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
 

 

