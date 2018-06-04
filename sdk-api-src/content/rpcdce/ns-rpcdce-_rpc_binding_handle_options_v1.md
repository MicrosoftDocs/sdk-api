---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

