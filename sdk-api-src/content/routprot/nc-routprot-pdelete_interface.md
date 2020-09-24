---
UID: NC:routprot.PDELETE_INTERFACE
title: PDELETE_INTERFACE (routprot.h)
description: The DeleteInterface function removes an interface from the set managed by the routing protocol.
helpviewer_keywords: ["DeleteInterface","DeleteInterface callback function [RAS]","PDELETE_INTERFACE","PDELETE_INTERFACE callback","_mpr_deleteinterface","routprot/DeleteInterface","rras.deleteinterface"]
old-location: rras\deleteinterface.htm
tech.root: RRAS
ms.assetid: 0b4c24d4-2588-412e-b3ec-dd73cbdac921
ms.date: 12/05/2018
ms.keywords: DeleteInterface, DeleteInterface callback function [RAS], PDELETE_INTERFACE, PDELETE_INTERFACE callback, _mpr_deleteinterface, routprot/DeleteInterface, rras.deleteinterface
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
 - PDELETE_INTERFACE
 - routprot/PDELETE_INTERFACE
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
 - DeleteInterface
---

# PDELETE_INTERFACE callback function


## -description

The 
<b>DeleteInterface</b> function removes an interface from the set managed by the routing protocol.

## -parameters

### -param InterfaceIndex [in]

Specifies the interface in the set of interfaces configured on the router.

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
The attempt to delete the interface failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>InterfaceIndex</i> parameter is invalid (for example, no interface exists with that index).

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/routprot/nc-routprot-padd_interface">AddInterface</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-functions">Routing Protocol Interface Functions</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>