---
UID: NS:rpcdce.RPC_IF_ID_VECTOR
title: RPC_IF_ID_VECTOR
author: windows-sdk-content
description: The RPC_IF_ID_VECTOR structure contains a list of interfaces offered by a server.
old-location: rpc\rpc_if_id_vector.htm
tech.root: Rpc
ms.assetid: 0bbef807-9eba-496b-be1c-4e48be7cc713
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RPC_IF_ID_VECTOR, RPC_IF_ID_VECTOR structure [RPC], _rpc_rpc_if_id_vector, rpc.rpc_if_id_vector, rpcdce/RPC_IF_ID_VECTOR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - RPC_IF_ID_VECTOR
product: Windows
targetos: Windows
req.typenames: RPC_IF_ID_VECTOR
req.redist: 
---

# RPC_IF_ID_VECTOR structure


## -description


The 
<b>RPC_IF_ID_VECTOR</b> structure contains a list of interfaces offered by a server.


## -struct-fields




### -field Count

Number of interface-identification structures present in the array <b>IfHandl</b>.


### -field IfId

 




#### - IfHandl

Array of pointers to interface-identification structures that contains <b>Count</b> elements.


## -remarks



The interface identification vector contains a count member (<b>Count</b>), followed by an array of pointers to interface identifiers (
<a href="https://msdn.microsoft.com/6fad80e0-4239-48f7-9cd1-3b9c56303346">RPC_IF_ID</a>).

The interface identification vector is a read-only vector. To obtain a vector of the interface identifiers registered by a server with the run-time library, an application calls 
<a href="https://msdn.microsoft.com/f6d89f2c-ff51-44ab-9f8a-2f76cd3ac6db">RpcMgmtInqIfIds</a>. To obtain a vector of the interface identifiers exported by a server, an application calls 
<a href="https://msdn.microsoft.com/92f33e1d-a054-4484-903a-c91d3cd549d1">RpcNsMgmtEntryInqIfIds</a>.

The RPC run-time library allocates memory for the interface identification vector. The application calls 
<a href="https://msdn.microsoft.com/1af518a7-02db-438a-ba3f-723bd8422188">RpcIfIdVectorFree</a> to free the interface identification vector.




## -see-also




<a href="https://msdn.microsoft.com/1af518a7-02db-438a-ba3f-723bd8422188">RpcIfIdVectorFree</a>



<a href="https://msdn.microsoft.com/f6d89f2c-ff51-44ab-9f8a-2f76cd3ac6db">RpcMgmtInqIfIds</a>



<a href="https://msdn.microsoft.com/92f33e1d-a054-4484-903a-c91d3cd549d1">RpcNsMgmtEntryInqIfIds</a>
 

 

