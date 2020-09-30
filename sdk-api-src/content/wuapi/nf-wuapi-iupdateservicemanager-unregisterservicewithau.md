---
UID: NF:wuapi.IUpdateServiceManager.UnregisterServiceWithAU
title: IUpdateServiceManager::UnregisterServiceWithAU (wuapi.h)
description: Unregisters a service with Automatic Updates.
helpviewer_keywords: ["IUpdateServiceManager interface [Windows Update Agent]","UnregisterServiceWithAU method","IUpdateServiceManager.UnregisterServiceWithAU","IUpdateServiceManager::UnregisterServiceWithAU","UnregisterServiceWithAU","UnregisterServiceWithAU method [Windows Update Agent]","UnregisterServiceWithAU method [Windows Update Agent]","IUpdateServiceManager interface","wua.iupdateservicemanager_unregisterservicewithau","wuapi/IUpdateServiceManager::UnregisterServiceWithAU"]
old-location: wua\iupdateservicemanager_unregisterservicewithau.htm
tech.root: wua
ms.assetid: d537594c-ccf3-463b-9860-612c5ea351cb
ms.date: 12/05/2018
ms.keywords: IUpdateServiceManager interface [Windows Update Agent],UnregisterServiceWithAU method, IUpdateServiceManager.UnregisterServiceWithAU, IUpdateServiceManager::UnregisterServiceWithAU, UnregisterServiceWithAU, UnregisterServiceWithAU method [Windows Update Agent], UnregisterServiceWithAU method [Windows Update Agent],IUpdateServiceManager interface, wua.iupdateservicemanager_unregisterservicewithau, wuapi/IUpdateServiceManager::UnregisterServiceWithAU
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
 - IUpdateServiceManager::UnregisterServiceWithAU
 - wuapi/IUpdateServiceManager::UnregisterServiceWithAU
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
 - IUpdateServiceManager.UnregisterServiceWithAU
---

# IUpdateServiceManager::UnregisterServiceWithAU


## -description

Unregisters a service with Automatic Updates.

## -parameters

### -param serviceID

An identifier for the service to be unregistered.

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
<dt><b>WU_E_DS_INVALIDOPERATION</b></dt>
</dl>
</td>
<td width="60%">
The state of Automatic Updates could not be changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_DS_UNKNOWNSERVICE</b></dt>
</dl>
</td>
<td width="60%">
Attempt to register an unknown service.

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
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_CALL_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The user canceled the change.

</td>
</tr>
</table>

## -remarks

This method returns <b>WU_E_DS_INVALIDOPERATION</b> if the requested change in the state of Automatic Updates is contrary to the specifications in the Authorization Cab. An error is returned by <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> function if the Authorization Cab has not been signed.

This method returns <b>WU_E_DS_UNKNOWNSERVICE</b> if the service to be removed does not exist.

This method returns <b>WU_E_DS_NEEDWINDOWSSERVICE</b> if you attempt to remove the Windows Update service and if it is the only service that is registered with Automatic Updates.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager">IUpdateServiceManager</a>