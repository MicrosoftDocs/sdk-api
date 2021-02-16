---
UID: NC:routprot.PDISCONNECT_CLIENT
title: PDISCONNECT_CLIENT (routprot.h)
description: The router manager calls the DisconnectClient function when a client disconnects from an interface on which the routing protocol is running.
helpviewer_keywords: ["DisconnectClient","DisconnectClient callback function [RAS]","PDISCONNECT_CLIENT","PDISCONNECT_CLIENT callback","_mpr_disconnectclient","routprot/DisconnectClient","rras.disconnectclient"]
old-location: rras\disconnectclient.htm
tech.root: RRAS
ms.assetid: 45859605-2981-4236-9546-9b88e07673fe
ms.date: 12/05/2018
ms.keywords: DisconnectClient, DisconnectClient callback function [RAS], PDISCONNECT_CLIENT, PDISCONNECT_CLIENT callback, _mpr_disconnectclient, routprot/DisconnectClient, rras.disconnectclient
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
 - PDISCONNECT_CLIENT
 - routprot/PDISCONNECT_CLIENT
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
 - DisconnectClient
---

# PDISCONNECT_CLIENT callback function


## -description

The router manager calls the 
<b>DisconnectClient</b> function when a client disconnects from an interface on which the routing protocol is running.

The <a href="/windows/desktop/api/routprot/ns-routprot-mpr50_routing_characteristics">PDISCONNECT_CLIENT</a> type defines a pointer to this callback function. <i>DisconnectClient</i> is a placeholder for the application-defined function name.

## -parameters

### -param InterfaceIndex [in]

Specifies the index of the interface on which the client is connecting.

### -param ClientAddress [in]

Pointer to the address (for example, the IP address) of the connecting client.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value should be one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the following is true: 




The <i>InterfaceIndex</i> parameter is invalid, for example, no interface exists with that index.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/routprot/nc-routprot-pconnect_client">ConnectClient</a>