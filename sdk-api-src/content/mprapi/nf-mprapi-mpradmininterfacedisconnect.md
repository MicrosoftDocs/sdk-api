---
UID: NF:mprapi.MprAdminInterfaceDisconnect
title: MprAdminInterfaceDisconnect function (mprapi.h)

description: The MprAdminInterfaceDisconnect function disconnects a connected WAN interface.
old-location: rras\mpradmininterfacedisconnect.htm
tech.root: RRAS
ms.assetid: 32499e2f-9c67-4314-adbf-75482a9d511e

ms.date: 12/05/2018
ms.keywords: MprAdminInterfaceDisconnect, MprAdminInterfaceDisconnect function [RAS], _mpr_mpradmininterfacedisconnect, mprapi/MprAdminInterfaceDisconnect, rras.mpradmininterfacedisconnect
ms.topic: function
f1_keywords: 
 - "mprapi/MprAdminInterfaceDisconnect"
dev_langs:
 - c++
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminInterfaceDisconnect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprAdminInterfaceDisconnect function


## -description


The 
<b>MprAdminInterfaceDisconnect</b> function disconnects a connected WAN interface.


## -parameters




### -param hMprServer [in]

Handle to the  router on which to execute this call. Obtain this handle by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.


### -param hInterface [in]

Handle to the interface. This handle is obtained from a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling application does not have sufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DDM_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Demand Dial Manager (DDM) is not running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hInterface</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INTERFACE_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
This interface is not connected. Therefore, it cannot be disconnected.

</td>
</tr>
</table>
 


<div> </div>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>, 
<a href="https://docs.microsoft.com/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfaceconnect">MprAdminInterfaceConnect</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>




