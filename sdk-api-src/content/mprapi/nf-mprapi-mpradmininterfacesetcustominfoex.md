---
UID: NF:mprapi.MprAdminInterfaceSetCustomInfoEx
title: MprAdminInterfaceSetCustomInfoEx function
author: windows-sdk-content
description: Sets the tunnel specific custom configuration for a specified demand dial interface on a specified server.
old-location: rras\mpradmininterfacesetcustominfoex.htm
tech.root: rras
ms.assetid: 306d9d6c-6196-4a1f-8549-f8dd0fb5ab6f
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: MprAdminInterfaceSetCustomInfoEx, MprAdminInterfaceSetCustomInfoEx function [RAS], mprapi/MprAdminInterfaceSetCustomInfoEx, rras.mpradmininterfacesetcustominfoex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - MprAdminInterfaceSetCustomInfoEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprAdminInterfaceSetCustomInfoEx function


## -description


Sets the tunnel specific custom configuration for a specified demand dial interface on a specified server.


## -parameters




### -param hMprServer [in]

The handle to the router to query. This handle is obtained by a previous call to the <a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a> function.


### -param hInterface [in]

The handle to the interface.  This handle is  obtained by a previous call to the <a href="https://msdn.microsoft.com/c9590ebe-7e49-4ad1-bd9b-0d9c51938bc4">MprAdminInterfaceCreate</a> function or the <a href="https://msdn.microsoft.com/a220dbc1-90e0-4290-8a65-c2a2dd218f07">MprAdminInterfaceGetHandle</a> function.


### -param pCustomInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/53c4b7ae-db73-4d97-a99f-a98354c48a92">MPR_IF_CUSTOMINFOEX</a>  structure that contains tunnel specific custom configuration.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>. If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hInterface</i> value is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCustomInfo</i> parameter is <b>NULL</b> or the interface type is not <b>ROUTER_IF_TYPE_FULL_ROUTER</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There were insufficient resources to complete the operation.

</td>
</tr>
</table>
 




## -remarks



If you need to delete the custom configuration for IKEv2 tunnel of an interface, call the  <b>MprAdminInterfaceSetCustomInfoEx</b> function with the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/53c4b7ae-db73-4d97-a99f-a98354c48a92">MPR_IF_CUSTOMINFOEX</a>   structure set to zero.

If you need to delete the IKEv2 main mode and quick mode policy configuration for an interface, set the <b>customPolicy</b> parameter of the <b>customIkev2Config</b> member in <a href="https://msdn.microsoft.com/53c4b7ae-db73-4d97-a99f-a98354c48a92">MPR_IF_CUSTOMINFOEX</a>   structure to <b>NULL</b>.

If you need to delete the certificate configured to be used during IKEv2 main mode SA negotiation, set the <b>cbData</b> member of <b>certificateName</b> in <b>customIkev2Config</b> member of <a href="https://msdn.microsoft.com/53c4b7ae-db73-4d97-a99f-a98354c48a92">MPR_IF_CUSTOMINFOEX</a>   structure to 0.




## -see-also




<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

