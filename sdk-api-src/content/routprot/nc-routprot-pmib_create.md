---
UID: NC:routprot.PMIB_CREATE
title: PMIB_CREATE (routprot.h)
description: The MibCreate function passes an SNMP MIB-style Create Request to the routing protocol.
helpviewer_keywords: ["MibCreate","MibCreate callback function [RAS]","PMIB_CREATE","PMIB_CREATE callback","_mpr_mibcreate","routprot/MibCreate","rras.mibcreate"]
old-location: rras\mibcreate.htm
tech.root: RRAS
ms.assetid: b3e8eca6-6d8d-4385-8c94-7269878810c0
ms.date: 12/05/2018
ms.keywords: MibCreate, MibCreate callback function [RAS], PMIB_CREATE, PMIB_CREATE callback, _mpr_mibcreate, routprot/MibCreate, rras.mibcreate
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
 - PMIB_CREATE
 - routprot/PMIB_CREATE
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
 - MibCreate
---

# PMIB_CREATE callback function


## -description

The 
<b>MibCreate</b> function passes an SNMP MIB-style Create Request to the routing protocol.

## -parameters

### -param InputDataSize [in]

Specifies the size of the data for the Create Request.

### -param InputData [in]

Pointer to a buffer that specifies the data for the Create Request.

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
Specifies the size or content of the data is inappropriate for the request.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/routprot/nc-routprot-pmib_delete">MibDelete</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-functions">Routing Protocol Interface Functions</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>