---
UID: NF:mprapi.MprAdminRegisterConnectionNotification
title: MprAdminRegisterConnectionNotification function (mprapi.h)
description: The MprAdminRegisterConnectionNotification function registers an event object with the Demand Dial Manager (DDM) so that, if an interface connects or disconnects, the event is signaled.
helpviewer_keywords: ["MprAdminRegisterConnectionNotification","MprAdminRegisterConnectionNotification function [RAS]","_mpr_mpradminregisterconnectionnotification","mprapi/MprAdminRegisterConnectionNotification","rras.mpradminregisterconnectionnotification"]
old-location: rras\mpradminregisterconnectionnotification.htm
tech.root: RRAS
ms.assetid: ba70154b-a2d1-4121-bea6-4572446bf9ee
ms.date: 12/05/2018
ms.keywords: MprAdminRegisterConnectionNotification, MprAdminRegisterConnectionNotification function [RAS], _mpr_mpradminregisterconnectionnotification, mprapi/MprAdminRegisterConnectionNotification, rras.mpradminregisterconnectionnotification
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
 - MprAdminRegisterConnectionNotification
 - mprapi/MprAdminRegisterConnectionNotification
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
 - MprAdminRegisterConnectionNotification
---

# MprAdminRegisterConnectionNotification function


## -description

The 
<b>MprAdminRegisterConnectionNotification</b> function registers an event object with the Demand Dial Manager (DDM) so that, if an interface connects or disconnects, the event is signaled.

## -parameters

### -param hMprServer [in]

Handle to the router on which to execute this call. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param hEventNotification [in]

Handle to an event object. This event is signaled whenever an interface connects or disconnects.

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

## -remarks

The event is signaled when an interface connects or disconnects. When an event is signaled, the calling application can determine which interface is affected by using a function such as 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a> or 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfaceenum">MprAdminInterfaceEnum</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminderegisterconnectionnotification">MprAdminDeregisterConnectionNotification</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfaceenum">MprAdminInterfaceEnum</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>