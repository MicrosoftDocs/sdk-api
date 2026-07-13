---
UID: NF:rpcdce.RpcServerInterfaceGroupCreateA
title: RpcServerInterfaceGroupCreateA function (rpcdce.h)
description: The RpcServerInterfaceGroupCreate function creates an RPC server interface group for the server application. (RpcServerInterfaceGroupCreateA)
helpviewer_keywords: ["RpcServerInterfaceGroupCreateA", "rpcdce/RpcServerInterfaceGroupCreateA"]
old-location: rpc\rpcserverinterfacegroupcreate.htm
tech.root: Rpc
ms.assetid: 7B648221-8256-42C9-B200-0EFD3B0DBA91
ms.date: 12/05/2018
ms.keywords: RpcServerInterfaceGroupCreate, RpcServerInterfaceGroupCreate function [RPC], RpcServerInterfaceGroupCreateA, RpcServerInterfaceGroupCreateW, rpc.rpcserverinterfacegroupcreate, rpcdce/RpcServerInterfaceGroupCreate, rpcdce/RpcServerInterfaceGroupCreateA, rpcdce/RpcServerInterfaceGroupCreateW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcServerInterfaceGroupCreateA
 - rpcdce/RpcServerInterfaceGroupCreateA
dev_langs:
 - c++
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
---

# RpcServerInterfaceGroupCreateA function


## -description

The <b>RpcServerInterfaceGroupCreate</b> function creates an RPC server interface group for the server application.  This interface group fully specifies the interfaces, endpoints, and idle properties of an RPC server application.  Once created, an interface group can be activated and deactivated as the application requires.

## -parameters

### -param Interfaces [in]

A pointer to an array of <a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_interface_template">RPC_INTERFACE_TEMPLATE</a> structures that define the interfaces exposed by the interface group.

### -param NumIfs [in]

The number of elements in <i>Interfaces</i>.

### -param Endpoints [in]

A pointer to an array of <a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_endpoint_template">RPC_ENDPOINT_TEMPLATE</a> structures that define the endpoints used by the interface group.

### -param NumEndpoints [in]

The number of elements in <i>Endpoints</i>.

### -param IdlePeriod [in]

The length of time in seconds after the interface group becomes idle that the RPC runtime should wait before invoking the idle callback.  0 means the callback is invoked immediately. <b>INFINITE</b> means the server application does not care about the interface group’s idle state.

### -param IdleCallbackFn [in]

A <a href="/windows/desktop/api/rpcdce/nc-rpcdce-rpc_interface_group_idle_callback_fn">RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN</a> callback that the RPC runtime will invoke once the interface group is idle for the length of time given in <i>IdlePeriod</i>.  Can be <b>NULL</b> only if <i>IdlePeriod</i> is <b>INFINITE</b>.

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
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

A server application can optionally be notified when an interface group becomes idle.  Though any application can take advantage of this functionality, it is targeted towards service developers who would like to enable their service to idle stop.

<i>IdlePeriod</i> prevents the RPC runtime from producing a large number of notifications if the idle state rapidly changes, and in the case of triggered services, helps the service avoid needlessly starting and stopping.  Developers should consider the cost of service initialization and shutdown, the expected frequency with which new activity will occur, and the cost of keeping the service sitting idle when selecting this value.   A low idle period will cause the service to frequently start and stop as new client activity takes place, whereas a high idle period will cause the service to consume resources without performing meaningful work.

Interfaces in an interface group can only be called over endpoints of the same group.  Interfaces that are not part of an interface group cannot be called over endpoints that are part of a group.

RPC server activity is not always visible to the server application.  In some cases, simply having a client with an open connection to the server may keep it active even if no calls have been dispatched for a long period of time.  Server applications must not rely on any correlation between the RPC runtime declaring that the group is idle and the time since the last call was dispatched.





> [!NOTE]
> The rpcdce.h header defines RpcServerInterfaceGroupCreate as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupactivate">RpcServerInterfaceGroupActivate</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupclose">RpcServerInterfaceGroupClose</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupdeactivate">RpcServerInterfaceGroupDeactivate</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupinqbindings">RpcServerInterfaceGroupInqBindings</a>
