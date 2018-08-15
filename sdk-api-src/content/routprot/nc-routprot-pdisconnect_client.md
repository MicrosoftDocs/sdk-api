---
UID: NC:routprot.PDISCONNECT_CLIENT
title: PDISCONNECT_CLIENT
author: windows-sdk-content
description: The router manager calls the DisconnectClient function when a client disconnects from an interface on which the routing protocol is running.
old-location: rras\disconnectclient.htm
old-project: rras
ms.assetid: 45859605-2981-4236-9546-9b88e07673fe
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DisconnectClient, DisconnectClient callback function [RAS], PDISCONNECT_CLIENT, PDISCONNECT_CLIENT callback, _mpr_disconnectclient, routprot/DisconnectClient, rras.disconnectclient
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: routprot.h
req.include-header: 
req.redist: 
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
 - DisconnectClient
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PDISCONNECT_CLIENT callback function


## -description


The router manager calls the 
<b>DisconnectClient</b> function when a client disconnects from an interface on which the routing protocol is running.

The <a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">PDISCONNECT_CLIENT</a> type defines a pointer to this callback function. <i>DisconnectClient</i> is a placeholder for the application-defined function name.


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




<a href="https://msdn.microsoft.com/548d8411-ca03-4316-9adb-3b4b48a740d9">ConnectClient</a>
 

 

