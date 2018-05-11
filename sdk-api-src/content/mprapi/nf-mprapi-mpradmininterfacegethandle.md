---
UID: NF:mprapi.MprAdminInterfaceGetHandle
title: MprAdminInterfaceGetHandle function
author: windows-driver-content
description: The MprAdminInterfaceGetHandle function retrieves a handle to a specified interface.
old-location: rras\mpradmininterfacegethandle.htm
old-project: RRAS
ms.assetid: a220dbc1-90e0-4290-8a65-c2a2dd218f07
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MprAdminInterfaceGetHandle, MprAdminInterfaceGetHandle function [RAS], _mpr_mpradmininterfacegethandle, mprapi/MprAdminInterfaceGetHandle, rras.mpradmininterfacegethandle
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
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Mprapi.dll
api_name:
-	MprAdminInterfaceGetHandle
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminInterfaceGetHandle function


## -description


The 
<b>MprAdminInterfaceGetHandle</b> function retrieves a handle to a specified interface.


## -parameters




### -param hMprServer [in]

Handle to the router on which to execute this call. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


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




<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>



<a href="https://msdn.microsoft.com/9b957ab0-0c5d-4478-914a-4837e6bbd56a">ROUTER_INTERFACE_TYPE</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

