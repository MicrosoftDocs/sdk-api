---
UID: NF:wuapi.IUpdateServiceManager.RemoveService
title: IUpdateServiceManager::RemoveService (wuapi.h)
description: Removes a service registration from Windows Update Agent (WUA).
helpviewer_keywords: ["IUpdateServiceManager interface [Windows Update Agent]","RemoveService method","IUpdateServiceManager.RemoveService","IUpdateServiceManager::RemoveService","RemoveService","RemoveService method [Windows Update Agent]","RemoveService method [Windows Update Agent]","IUpdateServiceManager interface","wua.iupdateservicemanager_removeservice","wuapi/IUpdateServiceManager::RemoveService"]
old-location: wua\iupdateservicemanager_removeservice.htm
tech.root: wua
ms.assetid: fedd0979-1cc1-40c7-93d1-ade2f069ee76
ms.date: 12/05/2018
ms.keywords: IUpdateServiceManager interface [Windows Update Agent],RemoveService method, IUpdateServiceManager.RemoveService, IUpdateServiceManager::RemoveService, RemoveService, RemoveService method [Windows Update Agent], RemoveService method [Windows Update Agent],IUpdateServiceManager interface, wua.iupdateservicemanager_removeservice, wuapi/IUpdateServiceManager::RemoveService
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
 - IUpdateServiceManager::RemoveService
 - wuapi/IUpdateServiceManager::RemoveService
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
 - IUpdateServiceManager.RemoveService
---

# IUpdateServiceManager::RemoveService


## -description

Removes a service registration from Windows Update Agent (WUA).

## -parameters

### -param serviceID [in]

An identifier for the service to be unregistered.

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
A parameter value was invalid.

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
The state of Automatic Updates could not be changed. This error is returned if you try to delete the service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_DS_UNKNOWNSERVICE</b></dt>
</dl>
</td>
<td width="60%">
Attempt to register  or remove an unknown service. 


</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager">IUpdateServiceManager</a>