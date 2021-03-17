---
UID: NC:routprot.PDO_UPDATE_ROUTES
title: PDO_UPDATE_ROUTES (routprot.h)
description: The DoUpdateRoutes function requests the routing protocol to perform a routing information update over the specified interface to obtain static route information.
helpviewer_keywords: ["DoUpdateRoutes","DoUpdateRoutes callback function [RAS]","PDO_UPDATE_ROUTES","PDO_UPDATE_ROUTES callback","_mpr_doupdateroutes","routprot/DoUpdateRoutes","rras.doupdateroutes"]
old-location: rras\doupdateroutes.htm
tech.root: RRAS
ms.assetid: 5942c856-f504-4e2d-86c8-f3207c787ed5
ms.date: 12/05/2018
ms.keywords: DoUpdateRoutes, DoUpdateRoutes callback function [RAS], PDO_UPDATE_ROUTES, PDO_UPDATE_ROUTES callback, _mpr_doupdateroutes, routprot/DoUpdateRoutes, rras.doupdateroutes
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
 - PDO_UPDATE_ROUTES
 - routprot/PDO_UPDATE_ROUTES
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
 - DoUpdateRoutes
---

# PDO_UPDATE_ROUTES callback function


## -description

The 
<b>DoUpdateRoutes</b> function requests the routing protocol to perform a routing information update over the specified interface to obtain static route information. (This process is called an autostatic route update.)

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
The update operation cannot be performed.

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

## -remarks

If the function returns NO_ERROR, the update operation started successfully on the interface. Check the routing protocol event queue for a completion event (see 
<a href="/windows/desktop/api/routprot/nc-routprot-pget_event_message">GetEventMessage</a>).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa374005(v=vs.85)">DoUpdateServices</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pget_event_message">GetEventMessage</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-functions">Routing Protocol Interface Functions</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>