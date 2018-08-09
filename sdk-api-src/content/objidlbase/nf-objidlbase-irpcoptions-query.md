---
UID: NF:objidlbase.IRpcOptions.Query
title: IRpcOptions::Query
author: windows-sdk-content
description: Retrieves the value of an RPC binding option property.
old-location: com\irpcoptions_query.htm
old-project: com
ms.assetid: 82f59cad-3718-4202-99d3-c3aafb8dbf56
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IRpcOptions interface [COM],Query method, IRpcOptions.Query, IRpcOptions::Query, Query, Query method [COM], Query method [COM],IRpcOptions interface, _com_irpcoptions_query, com.irpcoptions_query, objidlbase/IRpcOptions::Query
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IRpcOptions.Query
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

