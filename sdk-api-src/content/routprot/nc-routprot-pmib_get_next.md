---
UID: NC:routprot.PMIB_GET_NEXT
title: PMIB_GET_NEXT
author: windows-sdk-content
description: The MibGetNext function passes a SNMP MIB-style Get Next Request to the routing protocol.
old-location: rras\mibgetnext.htm
old-project: RRAS
ms.assetid: 00047426-11b6-4b68-8a44-45608611eafe
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: MibGetNext, MibGetNext callback function [RAS], PMIB_GET_NEXT, PMIB_GET_NEXT callback, _mpr_mibgetnext, routprot/MibGetNext, rras.mibgetnext
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Routprot.h
api_name:
 - MibGetNext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PMIB_GET_NEXT callback function


## -description


The 
<b>MibGetNext</b> function passes a SNMP MIB-style Get Next Request to the routing protocol.


## -parameters




### -param InputDataSize [in]

Specifies the size of the data for the Get Next Request.


### -param InputData [in]

Pointer to the data for the Get Next Request.


### -param OutputDataSize [out]

Pointer to a <b>ULONG</b> variable: 




On input: This variable that contains the size of the output buffer.

On output: This variable contains the size of data placed in the output buffer. If the initial size was not large enough, the variable contains the buffer size required to hold all of the output data.


### -param OutputData [out]

Pointer to a buffer that receives the data from the MIB entry.


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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of the output buffer provided is not large enough to hold the requested information. The required size is returned in the <b>ULONG</b> variable pointed to by the <i>OutputDataSize</i> parameter.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/a6f3d450-0ca1-4c22-9e48-addf317cac2a">MibGet</a>



<a href="https://msdn.microsoft.com/3aef09e2-6314-4de8-a9dd-e02c13e0145c">MibGetFirst</a>



<a href="https://msdn.microsoft.com/f1df3476-f6c5-4f7e-bc86-83e5f8d0cd57">MibSet</a>



<a href="https://msdn.microsoft.com/fd780458-ef23-4ef2-8fe8-29b32100917f">Routing Protocol Interface Functions</a>



<a href="https://msdn.microsoft.com/0429f5ca-6574-48f5-85ab-70b4677ca539">Routing Protocol Interface Reference</a>
 

 

