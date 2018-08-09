---
UID: NF:rpcdce.RpcIfInqId
title: RpcIfInqId function
author: windows-sdk-content
description: The RpcIfInqId function returns the interface-identification part of an interface specification.
old-location: rpc\rpcifinqid.htm
old-project: rpc
ms.assetid: 1b91e88c-b242-472f-b719-60f96599cb67
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RpcIfInqId, RpcIfInqId function [RPC], _rpc_rpcifinqid, rpc.rpcifinqid, rpcdce/RpcIfInqId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
tech.root: 
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcIfInqId
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcIfInqId function


## -description


The 
<b>RpcIfInqId</b> function returns the interface-identification part of an interface specification.


## -parameters




### -param RpcIfHandle

Stub-generated structure specifying the interface to query.


### -param RpcIfId

Returns a pointer to the interface identification. The application provides memory for the returned data.


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



An application calls the 
<b>RpcIfInqId</b> function to obtain a copy of the interface identification from the provided interface specification.

The returned interface identification consists of the interface UUID and interface version numbers (major and minor) specified in the <i>IfSpec</i> parameter from the IDL file.




## -see-also




<a href="https://msdn.microsoft.com/4c5f86a5-7867-4d5a-a255-5c0c57c7fe0a">RpcServerInqIf</a>



<a href="https://msdn.microsoft.com/f7f6a7c3-ce6c-4b8b-9853-596c39a0e76d">RpcServerRegisterIf</a>
 

 

