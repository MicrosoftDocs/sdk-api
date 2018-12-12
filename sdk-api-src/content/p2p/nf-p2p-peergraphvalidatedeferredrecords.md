---
UID: NF:p2p.PeerGraphValidateDeferredRecords
title: PeerGraphValidateDeferredRecords function
author: windows-sdk-content
description: The PeerGraphValidateDeferredRecords function indicates to the Peer Graphing Infrastructure that it is time to resubmit any deferred records for the security module to validate.
old-location: p2p\peergraphvalidatedeferredrecords.htm
tech.root: P2PSdk
ms.assetid: a9a48d8a-f31e-4526-bd09-826f04a564b1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PeerGraphValidateDeferredRecords, PeerGraphValidateDeferredRecords function [Peer Networking], p2p.peergraphvalidatedeferredrecords, p2p/PeerGraphValidateDeferredRecords
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2PGraph.dll
api_name:
 - PeerGraphValidateDeferredRecords
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerGraphValidateDeferredRecords function


## -description


The <b>PeerGraphValidateDeferredRecords</b> function indicates to the Peer Graphing Infrastructure that it is time to resubmit any deferred records for the   security module to validate.


## -parameters




### -param hGraph [in]

Handle to the peer graph.


### -param cRecordIds [in]

Specifies the number  of records specified in <i>pRecordIds</i>.  Specify zero (0) to instruct the Graphing infrastructure to validate all deferred records. If zero (0) is specified, <i>pRecordIds</i> is ignored.


### -param pRecordIds [in]

Pointer to  an array of record IDs to validate.


## -returns



If the function call succeeds, the return value is <b>S_OK</b>. Otherwise, it  returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to perform the specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The handle to the peer graph is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The peer graph must be  initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -remarks



When a new record comes to the computer from its  neighbor in the peer graph, the Peer Graphing Infrastructure  attempts to validate the record by calling  the <a href="https://msdn.microsoft.com/5d81f09b-e46b-43e6-b0a8-ed7c236f2968">PFNPEER_VALIDATE_RECORD</a> callback, specified in the <a href="https://msdn.microsoft.com/b4331cfc-dc1a-490b-b21d-0550f1d3fe33">PEER_SECURITY_INTERFACE</a> structure during a call to either <a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a> or <a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>.  If the security module does not  have all the information necessary to validate the record, it returns the  PEER_E_DEFERRED_VALIDATION error.  Once the security module obtains enough information, it must then validate the records using <b>PeerGraphValidateDeferredRecords</b>. When this function is called, the Peer Graphing Infrastructure calls <i>PFNPEER_VALIDATE_RECORD</i> to validate the records with IDs in <i>pRecordIds</i>.




## -see-also




<a href="https://msdn.microsoft.com/b4331cfc-dc1a-490b-b21d-0550f1d3fe33">PEER_SECURITY_INTERFACE</a>



<a href="https://msdn.microsoft.com/5d81f09b-e46b-43e6-b0a8-ed7c236f2968">PFNPEER_VALIDATE_RECORD</a>



<a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a>



<a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>
 

 

