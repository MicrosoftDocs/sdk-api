---
UID: NS:rpcdce.RPC_IF_ID_VECTOR
title: RPC_IF_ID_VECTOR (rpcdce.h)
description: The RPC_IF_ID_VECTOR structure contains a list of interfaces offered by a server.
helpviewer_keywords: ["RPC_IF_ID_VECTOR","RPC_IF_ID_VECTOR structure [RPC]","_rpc_rpc_if_id_vector","rpc.rpc_if_id_vector","rpcdce/RPC_IF_ID_VECTOR"]
old-location: rpc\rpc_if_id_vector.htm
tech.root: Rpc
ms.assetid: 0bbef807-9eba-496b-be1c-4e48be7cc713
ms.date: 12/05/2018
ms.keywords: RPC_IF_ID_VECTOR, RPC_IF_ID_VECTOR structure [RPC], _rpc_rpc_if_id_vector, rpc.rpc_if_id_vector, rpcdce/RPC_IF_ID_VECTOR
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
targetos: Windows
req.typenames: RPC_IF_ID_VECTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RPC_IF_ID_VECTOR
 - rpcdce/RPC_IF_ID_VECTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcdce.h
api_name:
 - RPC_IF_ID_VECTOR
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
<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_if_id">RPC_IF_ID</a>).

The interface identification vector is a read-only vector. To obtain a vector of the interface identifiers registered by a server with the run-time library, an application calls 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtinqifids">RpcMgmtInqIfIds</a>. To obtain a vector of the interface identifiers exported by a server, an application calls 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmtentryinqifidsa">RpcNsMgmtEntryInqIfIds</a>.

The RPC run-time library allocates memory for the interface identification vector. The application calls 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcifidvectorfree">RpcIfIdVectorFree</a> to free the interface identification vector.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcifidvectorfree">RpcIfIdVectorFree</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtinqifids">RpcMgmtInqIfIds</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmtentryinqifidsa">RpcNsMgmtEntryInqIfIds</a>

