---
UID: NC:routprot.PMIB_DELETE
title: PMIB_DELETE
author: windows-driver-content
description: The MibDelete function passes an SNMP MIB-style Delete Request to the routing protocol.
old-location: rras\mibdelete.htm
old-project: RRAS
ms.assetid: 3097843e-ffa6-443a-9ee8-1034f3ed474a
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: MibDelete, MibDelete callback function [RAS], PMIB_DELETE, PMIB_DELETE callback, _mpr_mibdelete, routprot/MibDelete, rras.mibdelete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: routprot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Routprot.h
api_name:
-	MibDelete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PMIB_DELETE callback function


## -description


The 
<b>MibDelete</b> function passes an SNMP MIB-style Delete Request to the routing protocol.


## -parameters




### -param InputDataSize [in]

Specifies the size of the data for the Delete Request.


### -param InputData [in]

Pointer to a buffer that specifies the data for the Delete Request.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The routing protocol could not complete the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The size or content of the data is inappropriate for the request.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/b3e8eca6-6d8d-4385-8c94-7269878810c0">MibCreate</a>



<a href="https://msdn.microsoft.com/fd780458-ef23-4ef2-8fe8-29b32100917f">Routing Protocol Interface Functions</a>



<a href="https://msdn.microsoft.com/0429f5ca-6574-48f5-85ab-70b4677ca539">Routing Protocol Interface Reference</a>
 

 

