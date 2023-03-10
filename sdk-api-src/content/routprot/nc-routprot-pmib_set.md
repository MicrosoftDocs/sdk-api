---
UID: NC:routprot.PMIB_SET
title: PMIB_SET (routprot.h)
description: The MibSet function passes a SNMP MIB-style Set Request to the routing protocol.
helpviewer_keywords: ["MibSet","PMIB_SET","PMIB_SET callback","PMIB_SET callback function [RAS]","TBD","_mpr_mibset","routprot/PMIB_SET","rras.mibset"]
old-location: rras\mibset.htm
tech.root: RRAS
ms.assetid: f1df3476-f6c5-4f7e-bc86-83e5f8d0cd57
ms.date: 12/05/2018
ms.keywords: MibSet, PMIB_SET, PMIB_SET callback, PMIB_SET callback function [RAS], TBD, _mpr_mibset, routprot/PMIB_SET, rras.mibset
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
 - PMIB_SET
 - routprot/PMIB_SET
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
 - PMIB_SET
---

# PMIB_SET callback function


## -description

The 
<b>MibSet</b> function passes a SNMP MIB-style Set Request to the routing protocol.

## -parameters

### -param InputDataSize [in]

Specifies the size of the data for the Set Request.

### -param InputData [in]

Pointer to a buffer that specifies the data for the Set Request.

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

<a href="/windows/desktop/api/routprot/nc-routprot-pmib_get">MibGet</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pmib_get_first">MibGetFirst</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pmib_get_next">MibGetNext</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-functions">Routing Protocol Interface Functions</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>