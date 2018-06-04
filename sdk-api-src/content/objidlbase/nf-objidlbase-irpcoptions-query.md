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

# IRpcOptions::Query


## -description


Retrieves the value of an RPC binding option property.


## -parameters




### -param pPrx [in]

A pointer to the proxy whose property is being queried.


### -param dwProperty [in]

An identifier of the property to be queried, which must be COMBND_RPCTIMEOUT or COMBND_SERVER_LOCALITY (this flag is available starting with Windows Server 2003.)


### -param pdwValue [out]

A pointer to the property value.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



While the COMBND_RPCTIMEOUT property can also be set using the <a href="https://msdn.microsoft.com/library/windows/hardware/ff544503">Set</a> method, the COMBND_SERVER_LOCALITY property can only be queried.

See <a href="https://msdn.microsoft.com/aa5db8ac-4c29-43cf-a7ed-a870df9dfb82">IRpcOptions</a> for a table of the possible values of the COMBND_RPCTIMEOUT property.

The possible values of the COMBND_SERVER_LOCALITY property, which describes the degree of remoteness of the RPC connection, are enumerated in the following table.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>SERVER_LOCALITY_PROCESS_LOCAL
</td>
<td>The counterpart is in the same process as the client.
</td>
</tr>
<tr>
<td>SERVER_LOCALITY_MACHINE_LOCAL
</td>
<td>The counterpart is on the same computer as the client but in a different process.
</td>
</tr>
<tr>
<td>SERVER_LOCALITY_REMOTE
</td>
<td>The counterpart is on a remote computer.
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/aa5db8ac-4c29-43cf-a7ed-a870df9dfb82">IRpcOptions</a>
 

 

