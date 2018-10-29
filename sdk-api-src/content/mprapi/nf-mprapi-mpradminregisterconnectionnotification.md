---
UID: NF:mprapi.MprAdminRegisterConnectionNotification
title: MprAdminRegisterConnectionNotification function
author: windows-sdk-content
description: The MprAdminRegisterConnectionNotification function registers an event object with the Demand Dial Manager (DDM) so that, if an interface connects or disconnects, the event is signaled.
old-location: rras\mpradminregisterconnectionnotification.htm
tech.root: RRAS
ms.assetid: ba70154b-a2d1-4121-bea6-4572446bf9ee
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: MprAdminRegisterConnectionNotification, MprAdminRegisterConnectionNotification function [RAS], _mpr_mpradminregisterconnectionnotification, mprapi/MprAdminRegisterConnectionNotification, rras.mpradminregisterconnectionnotification
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
 - MprAdminRegisterConnectionNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprAdminRegisterConnectionNotification function


## -description


The 
<b>MprAdminRegisterConnectionNotification</b> function registers an event object with the Demand Dial Manager (DDM) so that, if an interface connects or disconnects, the event is signaled.


## -parameters




### -param hMprServer [in]

Handle to the router on which to execute this call. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


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
<a href="_win32_formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



The event is signaled when an interface connects or disconnects. When an event is signaled, the calling application can determine which interface is affected by using a function such as 
<a href="https://msdn.microsoft.com/27be536e-0437-4e30-aef7-ed92f50baeaa">MprAdminConnectionEnum</a> or 
<a href="https://msdn.microsoft.com/50486ad3-2f1d-4ab9-9a7f-7b72128486fb">MprAdminInterfaceEnum</a>.




## -see-also




<a href="_win32_formatmessage">FormatMessage</a>



<a href="https://msdn.microsoft.com/27be536e-0437-4e30-aef7-ed92f50baeaa">MprAdminConnectionEnum</a>



<a href="https://msdn.microsoft.com/72918a54-8e8a-404a-9fd3-45b0bcc98038">MprAdminDeregisterConnectionNotification</a>



<a href="https://msdn.microsoft.com/50486ad3-2f1d-4ab9-9a7f-7b72128486fb">MprAdminInterfaceEnum</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

