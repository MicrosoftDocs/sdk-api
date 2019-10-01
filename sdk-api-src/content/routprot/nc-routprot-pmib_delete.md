---
UID: NC:routprot.PMIB_DELETE
title: PMIB_DELETE (routprot.h)
author: windows-sdk-content
description: The MibDelete function passes an SNMP MIB-style Delete Request to the routing protocol.
old-location: rras\mibdelete.htm
tech.root: RRAS
ms.assetid: 3097843e-ffa6-443a-9ee8-1034f3ed474a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MibDelete, MibDelete callback function [RAS], PMIB_DELETE, PMIB_DELETE callback, _mpr_mibdelete, routprot/MibDelete, rras.mibdelete
ms.topic: callback
f1_keywords: 
 - "routprot/MibDelete"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Routprot.h
api_name:
 - MibDelete
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/routprot/nc-routprot-pmib_create">MibCreate</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/routing-protocol-interface-functions">Routing Protocol Interface Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>
 

 

