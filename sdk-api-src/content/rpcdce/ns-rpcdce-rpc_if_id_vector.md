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
 

 

