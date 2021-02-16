---
UID: NC:routprot.PMIB_GET_FIRST
title: PMIB_GET_FIRST (routprot.h)
description: The MibGetFirst function passes a SNMP MIB-style Get First Request to the routing protocol.
helpviewer_keywords: ["MibGetFirst","MibGetFirst callback function [RAS]","PMIB_GET_FIRST","PMIB_GET_FIRST callback","_mpr_mibgetfirst","routprot/MibGetFirst","rras.mibgetfirst"]
old-location: rras\mibgetfirst.htm
tech.root: RRAS
ms.assetid: 3aef09e2-6314-4de8-a9dd-e02c13e0145c
ms.date: 12/05/2018
ms.keywords: MibGetFirst, MibGetFirst callback function [RAS], PMIB_GET_FIRST, PMIB_GET_FIRST callback, _mpr_mibgetfirst, routprot/MibGetFirst, rras.mibgetfirst
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PMIB_GET_FIRST
 - routprot/PMIB_GET_FIRST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Routprot.h
api_name:
 - MibGetFirst
---

# PMIB_GET_FIRST callback function


## -description

The 
<b>MibGetFirst</b> function passes a SNMP MIB-style Get First Request to the routing protocol.

## -parameters

### -param InputDataSize [in]

Specifies the size of the data for the Get First Request.

### -param InputData [in]

Pointer to the data to be passed with the Get First Request.

### -param OutputDataSize [out]

Pointer to a <b>ULONG</b> variable: 




On input: This variable contains the size of the output buffer.

On output: This variable contains the size of the data placed in the output buffer. If the initial size was not large enough, the variable contains the buffer size required to hold all of the output data.

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

<a href="/windows/desktop/api/routprot/nc-routprot-pmib_get">MibGet</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pmib_get_next">MibGetNext</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pmib_set">MibSet</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-functions">Routing Protocol Interface Functions</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>