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
 

 

