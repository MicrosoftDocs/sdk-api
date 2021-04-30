---
UID: NF:mprapi.MprAdminInterfaceDelete
title: MprAdminInterfaceDelete function (mprapi.h)
description: The MprAdminInterfaceDelete function deletes an interface on a specified server.
helpviewer_keywords: ["MprAdminInterfaceDelete","MprAdminInterfaceDelete function [RAS]","_mpr_mpradmininterfacedelete","mprapi/MprAdminInterfaceDelete","rras.mpradmininterfacedelete"]
old-location: rras\mpradmininterfacedelete.htm
tech.root: RRAS
ms.assetid: a02fff1d-c0e0-4a00-b77e-33cc45850bc6
ms.date: 12/05/2018
ms.keywords: MprAdminInterfaceDelete, MprAdminInterfaceDelete function [RAS], _mpr_mpradmininterfacedelete, mprapi/MprAdminInterfaceDelete, rras.mpradmininterfacedelete
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprAdminInterfaceDelete
 - mprapi/MprAdminInterfaceDelete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminInterfaceDelete
---

# MprAdminInterfaceDelete function


## -description

The 
<b>MprAdminInterfaceDelete</b> function deletes an interface on a specified server.

## -parameters

### -param hMprServer [in]

Handle to the router on which to execute this call. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param hInterface [in]

Handle to the interface to delete. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>.

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
<dt><b>ERROR_INTERFACE_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The interface specified is a demand-dial interface and is currently connected.

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
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>