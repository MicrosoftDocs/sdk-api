---
UID: NF:mprapi.MprAdminInterfaceConnect
title: MprAdminInterfaceConnect function (mprapi.h)
description: The MprAdminInterfaceConnect function creates a connection to the specified WAN interface.
helpviewer_keywords: ["MprAdminInterfaceConnect","MprAdminInterfaceConnect function [RAS]","_mpr_mpradmininterfaceconnect","mprapi/MprAdminInterfaceConnect","rras.mpradmininterfaceconnect"]
old-location: rras\mpradmininterfaceconnect.htm
tech.root: RRAS
ms.assetid: 21440495-9372-42c7-8e40-8f3d5812f187
ms.date: 12/05/2018
ms.keywords: MprAdminInterfaceConnect, MprAdminInterfaceConnect function [RAS], _mpr_mpradmininterfaceconnect, mprapi/MprAdminInterfaceConnect, rras.mpradmininterfaceconnect
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
 - MprAdminInterfaceConnect
 - mprapi/MprAdminInterfaceConnect
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
 - MprAdminInterfaceConnect
---

# MprAdminInterfaceConnect function


## -description

The 
<b>MprAdminInterfaceConnect</b> function creates a connection to the specified WAN interface.

## -parameters

### -param hMprServer [in]

Handle to the router on which to execute this call. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param hInterface [in]

Handle to the interface. This handle is obtained from a previous call to 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>.

### -param hEvent [in]

Handle to an event that is signaled after the attempt to connect the interface has completed. The function initiates the connection attempt and returns immediately. After the event is signaled, you can obtain the result of the connection attempt by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetinfo">MprAdminInterfaceGetInfo</a>. 




If this parameter is <b>NULL</b>, and <i>fBlocking</i> is <b>TRUE</b>, then this call is synchronous, that is, the function does not return until the connection attempt has completed.

The calling application must specify <b>NULL</b> for this parameter, if <i>hMprServer</i> specifies a remote router.

### -param fSynchronous [in]

If <i>hEvent</i> is <b>NULL</b> and this parameter is set to <b>TRUE</b>, the function does not return until the connection attempt has completed. 




If <i>hEvent</i> is <b>NULL</b>, and this parameter is set to <b>FALSE</b>, the function will return immediately. A return value of PENDING indicates that the connection attempt was initiated successfully.

If <i>hEvent</i> is not <b>NULL</b>, this parameter is ignored.

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
<dt><b>ERROR_ALREADY_CONNECTING</b></dt>
</dl>
</td>
<td width="60%">
A connection is already in progress on this interface.

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
<dt><b>ERROR_INTERFACE_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The interface is currently disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INTERFACE_HAS_NO_DEVICES</b></dt>
</dl>
</td>
<td width="60%">
No adapters are available for this interface.

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
<dt><b>ERROR_SERVICE_IS_PAUSED</b></dt>
</dl>
</td>
<td width="60%">
The Demand Dial service is currently paused.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PENDING</b></dt>
</dl>
</td>
<td width="60%">
The interface is in the process of connecting. The calling application must wait on the <i>hEvent</i> handle, if one was specified. After the event is signaled, you can obtain the state of the connection and any associated error by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetinfo">MprAdminInterfaceGetInfo</a>.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The following table summarizes the relationship between <i>hEvent</i> and <i>fBlocking</i>.

<table>
<tr>
<th>hEvent</th>
<th>fBlocking</th>
<th>Result</th>
</tr>
<tr>
<td>Event Handle</td>
<td>Ignored</td>
<td>The call returns immediately. A return value of PENDING indicates that the attempt was initiated successfully. Wait on <i>hEvent</i>. When <i>hEvent</i> is signaled, use 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetinfo">MprAdminInterfaceGetInfo</a> to determine the success or failure of the connection attempt.</td>
</tr>
<tr>
<td><b>NULL</b></td>
<td><b>TRUE</b></td>
<td>The call does not return until the connection attempt has completed.</td>
</tr>
<tr>
<td><b>NULL</b></td>
<td><b>FALSE</b></td>
<td>The call returns immediately. A return value of PENDING indicates that the attempt was initiated successfully.</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacedisconnect">MprAdminInterfaceDisconnect</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetinfo">MprAdminInterfaceGetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>