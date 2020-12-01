---
UID: NF:mprapi.MprAdminInterfaceGetHandle
title: MprAdminInterfaceGetHandle function (mprapi.h)
description: The MprAdminInterfaceGetHandle function retrieves a handle to a specified interface.
helpviewer_keywords: ["MprAdminInterfaceGetHandle","MprAdminInterfaceGetHandle function [RAS]","_mpr_mpradmininterfacegethandle","mprapi/MprAdminInterfaceGetHandle","rras.mpradmininterfacegethandle"]
old-location: rras\mpradmininterfacegethandle.htm
tech.root: RRAS
ms.assetid: a220dbc1-90e0-4290-8a65-c2a2dd218f07
ms.date: 12/05/2018
ms.keywords: MprAdminInterfaceGetHandle, MprAdminInterfaceGetHandle function [RAS], _mpr_mpradmininterfacegethandle, mprapi/MprAdminInterfaceGetHandle, rras.mpradmininterfacegethandle
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
 - MprAdminInterfaceGetHandle
 - mprapi/MprAdminInterfaceGetHandle
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
 - MprAdminInterfaceGetHandle
---

# MprAdminInterfaceGetHandle function


## -description

The 
<b>MprAdminInterfaceGetHandle</b> function retrieves a handle to a specified interface.

## -parameters

### -param hMprServer [in]

Handle to the router on which to execute this call. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param lpwsInterfaceName [in]

Pointer to a <b>null</b>-terminated Unicode string that specifies the name of the interface to be retrieved.

### -param phInterface [out]

Pointer to a <b>HANDLE</b> variable that receives a handle to the interface specified by <i>lpwsInterfaceName</i>.

### -param fIncludeClientInterfaces [in]

Specifies whether the function returns a client interface. If this parameter is <b>FALSE</b>, interfaces of type <b>ROUTER_IF_TYPE_CLIENT</b> are ignored in the search for the interface with the name specified by <i>lpwsInterfaceName</i>. If this parameter is <b>TRUE</b> and an interface with the specified name exists, 
<b>MprAdminInterfaceGetHandle</b> returns a handle to an interface of type <b>ROUTER_IF_TYPE_CLIENT</b>. Since it is possible that there are several interfaces of type <b>ROUTER_IF_TYPE_CLIENT</b>, the handle returned references the first interface found with the name specified by <i>lpwsInterfaceName</i>.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

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
<dt><b>ERROR_NO_SUCH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
No interface exists with the name specified by <i>lpwsInterfaceName</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The passed in handle to the server is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_NULL_REF_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>lpwsInterfaceName</i> is <b>NULL</b>.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/api/mprapi/ne-mprapi-router_interface_type">ROUTER_INTERFACE_TYPE</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>