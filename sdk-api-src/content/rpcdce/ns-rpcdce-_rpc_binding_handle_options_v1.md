---
UID: NS:rpcdce._RPC_BINDING_HANDLE_OPTIONS_V1
title: "_RPC_BINDING_HANDLE_OPTIONS_V1"
author: windows-sdk-content
description: Contains additional options with which to create an RPC binding handle.
old-location: rpc\rpc_binding_handle_options_v1.htm
tech.root: Rpc
ms.assetid: e2bd03cf-4d45-449f-9434-ec8ef405737b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PRPC_BINDING_HANDLE_OPTIONS_V1, RPC_BHO_DONTLINGER, RPC_BHO_NONCAUSAL, RPC_BINDING_HANDLE_OPTIONS, RPC_BINDING_HANDLE_OPTIONS structure [RPC], RPC_BINDING_HANDLE_OPTIONS_V1, RPC_BINDING_HANDLE_OPTIONS_V1 structure [RPC], _RPC_BINDING_HANDLE_OPTIONS_V1, rpc.rpc_binding_handle_options_v1, rpcdce/RPC_BINDING_HANDLE_OPTIONS, rpcdce/RPC_BINDING_HANDLE_OPTIONS_V1"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcdce.h
api_name:
 - RPC_BINDING_HANDLE_OPTIONS_V1
product: Windows
targetos: Windows
req.typenames: RPC_BINDING_HANDLE_OPTIONS_V1, *PRPC_BINDING_HANDLE_OPTIONS_V1
req.redist: 
---

# _RPC_BINDING_HANDLE_OPTIONS_V1 structure


## -description


The <b>RPC_BINDING_HANDLE_OPTIONS_V1</b> structure contains additional options with which to create an RPC binding handle.


## -struct-fields




### -field Version

The version of this structure. For <b>RPC_BINDING_HANDLE_OPTIONS_V1</b> this must be set to 1.


### -field Flags

A set of flags describing specific RPC behaviors. This parameter can be set to one or more of the following values. Note that by default, RPC calls use causal order and socket lingering.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_BHO_NONCAUSAL"></a><a id="rpc_bho_noncausal"></a><dl>
<dt><b>RPC_BHO_NONCAUSAL</b></dt>
</dl>
</td>
<td width="60%">
Specifies causal ordering whereby calls are executed independently of one another rather than in order of submission.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_BHO_DONTLINGER"></a><a id="rpc_bho_dontlinger"></a><dl>
<dt><b>RPC_BHO_DONTLINGER</b></dt>
</dl>
</td>
<td width="60%">
Specifies that a socket association must be shutdown after the last binding handle on it is freed.

</td>
</tr>
</table>
 


### -field ComTimeout

The communication timeout value, specified in microseconds. The default value for RPC is RPC_C_BINDING_DEFAULT_TIMEOUT. This option can be changed later by calling <a href="https://msdn.microsoft.com/3ea6fe6a-2064-4f53-852a-041281b62bbd">RpcMgmtSetComTimeout</a>.


### -field CallTimeout

The call timeout value, specified in microseconds. The default value for RPC is 0.


## -remarks



If this structure is not specified in a call to <a href="https://msdn.microsoft.com/0188512e-bff6-414b-a6eb-19bfe8e0b3a9">RpcBindingCreate</a>, the default values for each option are used.




## -see-also




<a href="https://msdn.microsoft.com/3e07d9e9-04d8-4f94-8104-cd0ee89a9407">RPC_BINDING_HANDLE</a>



<a href="https://msdn.microsoft.com/dbc73a66-b1ca-4a53-b662-430b611f8c20">RpcBindingBind</a>



<a href="https://msdn.microsoft.com/0188512e-bff6-414b-a6eb-19bfe8e0b3a9">RpcBindingCreate</a>
 

 

