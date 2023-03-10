---
UID: NC:routprot.PMIB_GET_NEXT
title: PMIB_GET_NEXT (routprot.h)
description: The MibGetNext function passes a SNMP MIB-style Get Next Request to the routing protocol.
helpviewer_keywords: ["MibGetNext","MibGetNext callback function [RAS]","PMIB_GET_NEXT","PMIB_GET_NEXT callback","_mpr_mibgetnext","routprot/MibGetNext","rras.mibgetnext"]
old-location: rras\mibgetnext.htm
tech.root: RRAS
ms.assetid: 00047426-11b6-4b68-8a44-45608611eafe
ms.date: 12/05/2018
ms.keywords: MibGetNext, MibGetNext callback function [RAS], PMIB_GET_NEXT, PMIB_GET_NEXT callback, _mpr_mibgetnext, routprot/MibGetNext, rras.mibgetnext
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
 - PMIB_GET_NEXT
 - routprot/PMIB_GET_NEXT
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
 - MibGetNext
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

<a href="/windows/desktop/api/routprot/nc-routprot-pmib_get">MibGet</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pmib_get_first">MibGetFirst</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pmib_set">MibSet</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-functions">Routing Protocol Interface Functions</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>