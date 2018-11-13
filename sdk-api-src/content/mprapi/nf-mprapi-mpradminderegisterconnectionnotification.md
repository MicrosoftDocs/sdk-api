---
UID: NF:mprapi.MprAdminDeregisterConnectionNotification
title: MprAdminDeregisterConnectionNotification function
author: windows-sdk-content
description: The MprAdminDeregisterConnectionNotification function deregisters an event object that was previously registered using MprAdminRegisterConnectionNotification. Once deregistered, this event is no longer signaled when an interface connects or disconnects.
old-location: rras\mpradminderegisterconnectionnotification.htm
tech.root: rras
ms.assetid: 72918a54-8e8a-404a-9fd3-45b0bcc98038
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MprAdminDeregisterConnectionNotification, MprAdminDeregisterConnectionNotification function [RAS], _mpr_mpradminderegisterconnectionnotification, mprapi/MprAdminDeregisterConnectionNotification, rras.mpradminderegisterconnectionnotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - MprAdminDeregisterConnectionNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprAdminDeregisterConnectionNotification function


## -description


The 
<b>MprAdminDeregisterConnectionNotification</b> function deregisters an event object that was previously registered using 
<a href="https://msdn.microsoft.com/ba70154b-a2d1-4121-bea6-4572446bf9ee">MprAdminRegisterConnectionNotification</a>. Once deregistered, this event is no longer signaled when an interface connects or disconnects.


## -parameters




### -param hMprServer [in]

Handle to the router on which to execute this call. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


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
<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a>



<a href="https://msdn.microsoft.com/ba70154b-a2d1-4121-bea6-4572446bf9ee">MprAdminRegisterConnectionNotification</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

