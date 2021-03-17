---
UID: NF:wuapi.IUpdateServiceManager.RegisterServiceWithAU
title: IUpdateServiceManager::RegisterServiceWithAU (wuapi.h)
description: Registers a service with Automatic Updates.
helpviewer_keywords: ["IUpdateServiceManager interface [Windows Update Agent]","RegisterServiceWithAU method","IUpdateServiceManager.RegisterServiceWithAU","IUpdateServiceManager::RegisterServiceWithAU","RegisterServiceWithAU","RegisterServiceWithAU method [Windows Update Agent]","RegisterServiceWithAU method [Windows Update Agent]","IUpdateServiceManager interface","wua.iupdateservicemanager_registerservicewithau","wuapi/IUpdateServiceManager::RegisterServiceWithAU"]
old-location: wua\iupdateservicemanager_registerservicewithau.htm
tech.root: wua
ms.assetid: ea54d96a-9ffb-4abd-a032-4dfcc7ba6403
ms.date: 12/05/2018
ms.keywords: IUpdateServiceManager interface [Windows Update Agent],RegisterServiceWithAU method, IUpdateServiceManager.RegisterServiceWithAU, IUpdateServiceManager::RegisterServiceWithAU, RegisterServiceWithAU, RegisterServiceWithAU method [Windows Update Agent], RegisterServiceWithAU method [Windows Update Agent],IUpdateServiceManager interface, wua.iupdateservicemanager_registerservicewithau, wuapi/IUpdateServiceManager::RegisterServiceWithAU
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
 - IUpdateServiceManager::RegisterServiceWithAU
 - wuapi/IUpdateServiceManager::RegisterServiceWithAU
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
 - IUpdateServiceManager.RegisterServiceWithAU
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

This method returns <b>WU_E_INVALID_OPERATION</b> if the method is called with an invalid service ID.  This method also returns <b>WU_E_INVALID_OPERATION</b> if the service ID is valid but the service can't register with Automatic Updates. That is,  the requested change in the state of Automatic Updates is contrary to the specifications in the authorization cabinet file (for example, <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateservice-get_canregisterwithau">CanRegisterWithAU</a> property is set to <b>FALSE</b>). An error is returned by <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> function if the authorization cabinet file has not been signed.



This method returns <b>WU_E_DS_NEEDWINDOWSSERVICE</b> if you try to remove the Windows Update service.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager">IUpdateServiceManager</a>