---
UID: NC:routprot.PCONNECT_CLIENT
title: PCONNECT_CLIENT (routprot.h)
description: The router manager calls the ConnectClient function when a client connects to an interface on which the routing protocol is running.
helpviewer_keywords: ["ConnectClient","ConnectClient callback function [RAS]","PCONNECT_CLIENT","PCONNECT_CLIENT callback","_mpr_connectclient","routprot/ConnectClient","rras.connectclient"]
old-location: rras\connectclient.htm
tech.root: RRAS
ms.assetid: 548d8411-ca03-4316-9adb-3b4b48a740d9
ms.date: 12/05/2018
ms.keywords: ConnectClient, ConnectClient callback function [RAS], PCONNECT_CLIENT, PCONNECT_CLIENT callback, _mpr_connectclient, routprot/ConnectClient, rras.connectclient
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
 - PCONNECT_CLIENT
 - routprot/PCONNECT_CLIENT
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
 - ConnectClient
---

# PCONNECT_CLIENT callback function


## -description

The router manager calls the 
<b>ConnectClient</b> function when a client connects to an interface on which the routing protocol is running.

The <a href="/windows/desktop/api/routprot/ns-routprot-mpr50_routing_characteristics">PCONNECT_CLIENT</a> type defines a pointer to this callback function. <i>ConnectClient</i> is a placeholder for the application-defined function name.

## -parameters

### -param InterfaceIndex [in]

Specifies the index of the interface on which the client is connecting.

### -param ClientAddress [in]

Pointer to the address (such as the IP address) of the connecting client.

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

<a href="/windows/desktop/api/routprot/nc-routprot-pdisconnect_client">DisconnectClient</a>