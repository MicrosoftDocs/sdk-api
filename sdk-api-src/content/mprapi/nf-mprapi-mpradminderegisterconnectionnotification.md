---
UID: NF:mprapi.MprAdminDeregisterConnectionNotification
title: MprAdminDeregisterConnectionNotification function (mprapi.h)
description: The MprAdminDeregisterConnectionNotification function deregisters an event object that was previously registered using MprAdminRegisterConnectionNotification. Once deregistered, this event is no longer signaled when an interface connects or disconnects.
helpviewer_keywords: ["MprAdminDeregisterConnectionNotification","MprAdminDeregisterConnectionNotification function [RAS]","_mpr_mpradminderegisterconnectionnotification","mprapi/MprAdminDeregisterConnectionNotification","rras.mpradminderegisterconnectionnotification"]
old-location: rras\mpradminderegisterconnectionnotification.htm
tech.root: RRAS
ms.assetid: 72918a54-8e8a-404a-9fd3-45b0bcc98038
ms.date: 12/05/2018
ms.keywords: MprAdminDeregisterConnectionNotification, MprAdminDeregisterConnectionNotification function [RAS], _mpr_mpradminderegisterconnectionnotification, mprapi/MprAdminDeregisterConnectionNotification, rras.mpradminderegisterconnectionnotification
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
 - MprAdminDeregisterConnectionNotification
 - mprapi/MprAdminDeregisterConnectionNotification
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
 - MprAdminDeregisterConnectionNotification
---

# MprAdminDeregisterConnectionNotification function


## -description

The 
<b>MprAdminDeregisterConnectionNotification</b> function deregisters an event object that was previously registered using 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminregisterconnectionnotification">MprAdminRegisterConnectionNotification</a>. Once deregistered, this event is no longer signaled when an interface connects or disconnects.

## -parameters

### -param hMprServer [in]

Handle to the router on which to execute this call. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param hEventNotification [in]

Handle to an event object to deregister. This event is no longer  signaled when an interface connects or disconnects.

## -returns

If the function is successful, the return value is NO_ERROR.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>hEventNotification</i> parameter is <b>NULL</b> or is an invalid handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminregisterconnectionnotification">MprAdminRegisterConnectionNotification</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>