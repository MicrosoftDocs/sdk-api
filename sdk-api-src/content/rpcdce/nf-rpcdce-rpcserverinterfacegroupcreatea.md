---
UID: NF:rpcdce.RpcServerInterfaceGroupCreateA
title: RpcServerInterfaceGroupCreateA function (rpcdce.h)
author: windows-sdk-content
description: The RpcServerInterfaceGroupCreate function creates an RPC server interface group for the server application.
old-location: rpc\rpcserverinterfacegroupcreate.htm
tech.root: Rpc
ms.assetid: 7B648221-8256-42C9-B200-0EFD3B0DBA91
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RpcServerInterfaceGroupCreate, RpcServerInterfaceGroupCreate function [RPC], RpcServerInterfaceGroupCreateA, RpcServerInterfaceGroupCreateW, rpc.rpcserverinterfacegroupcreate, rpcdce/RpcServerInterfaceGroupCreate, rpcdce/RpcServerInterfaceGroupCreateA, rpcdce/RpcServerInterfaceGroupCreateW
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcServerInterfaceGroupCreateW (Unicode) and RpcServerInterfaceGroupCreateA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcServerInterfaceGroupCreate
 - RpcServerInterfaceGroupCreateA
 - RpcServerInterfaceGroupCreateW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RpcServerInterfaceGroupCreateA function


## -description


The <b>RpcServerInterfaceGroupCreate</b> function creates an RPC server interface group for the server application.  This interface group fully specifies the interfaces, endpoints, and idle properties of an RPC server application.  Once created, an interface group can be activated and deactivated as the application requires.


## -parameters




### -param Interfaces [in]

A pointer to an array of <a href="https://msdn.microsoft.com/4DBD0B43-659B-4074-954B-FE9ABB0DCE63">RPC_INTERFACE_TEMPLATE</a> structures that define the interfaces exposed by the interface group.


### -param NumIfs [in]

The number of elements in <i>Interfaces</i>.


### -param Endpoints [in]

A pointer to an array of <a href="https://msdn.microsoft.com/F1C4A10B-D7DA-4A2A-B166-F814E6926ADD">RPC_ENDPOINT_TEMPLATE</a> structures that define the endpoints used by the interface group.


### -param NumEndpoints [in]

The number of elements in <i>Endpoints</i>.


### -param IdlePeriod [in]

The length of time in seconds after the interface group becomes idle that the RPC runtime should wait before invoking the idle callback.  0 means the callback is invoked immediately. <b>INFINITE</b> means the server application does not care about the interface group’s idle state.


### -param IdleCallbackFn [in]

A <a href="https://msdn.microsoft.com/D34F2902-80EE-4011-A837-2A8C21E5A136">RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN</a> callback that the RPC runtime will invoke once the interface group is idle for the length of time given in <i>IdlePeriod</i>.  Can be <b>NULL</b> only if <i>IdlePeriod</i> is <b>INFINITE</b>.


### -param IdleCallbackContext [in]

A user-defined pointer to be passed to the idle callback in <i>IdleCallbackFn</i>.


### -param IfGroup [out]

If successful, a pointer to an <b>RPC_INTERFACE_GROUP</b> buffer that receives the handle to the newly created interface group.  If this function fails, <i>IfGroup</i> is undefined.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



A server application can optionally be notified when an interface group becomes idle.  Though any application can take advantage of this functionality, it is targeted towards service developers who would like to enable their service to idle stop.

<i>IdlePeriod</i> prevents the RPC runtime from producing a large number of notifications if the idle state rapidly changes, and in the case of triggered services, helps the service avoid needlessly starting and stopping.  Developers should consider the cost of service initialization and shutdown, the expected frequency with which new activity will occur, and the cost of keeping the service sitting idle when selecting this value.   A low idle period will cause the service to frequently start and stop as new client activity takes place, whereas a high idle period will cause the service to consume resources without performing meaningful work.

Interfaces in an interface group can only be called over endpoints of the same group.  Interfaces that are not part of an interface group cannot be called over endpoints that are part of a group.

RPC server activity is not always visible to the server application.  In some cases, simply having a client with an open connection to the server may keep it active even if no calls have been dispatched for a long period of time.  Server applications must not rely on any correlation between the RPC runtime declaring that the group is idle and the time since the last call was dispatched.




## -see-also




<a href="https://msdn.microsoft.com/A467DDEC-BEB1-4050-B540-4A1E819E7373">RpcServerInterfaceGroupActivate</a>



<a href="https://msdn.microsoft.com/DD7F12FC-EDB3-48C3-A87D-9ABAB4EFA009">RpcServerInterfaceGroupClose</a>



<a href="https://msdn.microsoft.com/625D8E6E-278F-4A96-879B-64294531D21B">RpcServerInterfaceGroupDeactivate</a>



<a href="https://msdn.microsoft.com/90535A05-9835-45F2-A62F-718736A80ED3">RpcServerInterfaceGroupInqBindings</a>
 

 

