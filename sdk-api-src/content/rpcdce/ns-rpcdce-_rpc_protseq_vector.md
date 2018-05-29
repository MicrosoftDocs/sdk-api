---
UID: NS:rpcdce._RPC_PROTSEQ_VECTOR
title: "_RPC_PROTSEQ_VECTOR"
author: windows-sdk-content
description: The RPC_PROTSEQ_VECTOR structure contains a list of protocol sequences the RPC run-time library uses to send and receive remote procedure calls.
old-location: rpc\rpc_protseq_vector.htm
old-project: Rpc
ms.assetid: 535ffce0-54e2-483c-8b74-006b6f5e05f0
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: RPC_PROTSEQ_VECTOR, RPC_PROTSEQ_VECTOR structure [RPC], _RPC_PROTSEQ_VECTOR, _rpc_rpc_protseq_vector, rpc.rpc_protseq_vector, rpcdce/RPC_PROTSEQ_VECTOR
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
req.typenames: RPC_PROTSEQ_VECTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Rpcdce.h
api_name:
-	RPC_PROTSEQ_VECTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _RPC_PROTSEQ_VECTOR structure


## -description


The 
<b>RPC_PROTSEQ_VECTOR</b> structure contains a list of protocol sequences the RPC run-time library uses to send and receive remote procedure calls.


## -struct-fields




### -field Count

Number of protocol-sequence strings present in the array <b>Protseq</b>.
					


### -field Protseq

Array of pointers to protocol-sequence strings. The number of pointers present is specified by the <b>Count</b> member.


## -remarks



The protocol-sequence vector contains a count member (<b>Count</b>), followed by an array of pointers to protocol-sequence strings (<b>Protseq</b>).

The protocol-sequence vector is a read-only vector. To obtain a protocol-sequence vector, a server application calls 
<a href="https://msdn.microsoft.com/7390e30a-9e29-417e-8d21-a045f1888036">RpcNetworkInqProtseqs</a>. The RPC run-time library allocates memory for the protocol-sequence vector. The server application calls 
<a href="https://msdn.microsoft.com/6f399600-0534-44cc-b179-d3bc7bee091d">RpcProtseqVectorFree</a> to free the protocol-sequence vector.




## -see-also




<a href="https://msdn.microsoft.com/7390e30a-9e29-417e-8d21-a045f1888036">RpcNetworkInqProtseqs</a>



<a href="https://msdn.microsoft.com/6f399600-0534-44cc-b179-d3bc7bee091d">RpcProtseqVectorFree</a>
 

 

