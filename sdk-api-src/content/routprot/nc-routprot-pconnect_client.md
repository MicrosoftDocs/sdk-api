---
UID: NC:routprot.PCONNECT_CLIENT
title: PCONNECT_CLIENT
author: windows-sdk-content
description: The router manager calls the ConnectClient function when a client connects to an interface on which the routing protocol is running.
old-location: rras\connectclient.htm
tech.root: RRAS
ms.assetid: 548d8411-ca03-4316-9adb-3b4b48a740d9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ConnectClient, ConnectClient callback function [RAS], PCONNECT_CLIENT, PCONNECT_CLIENT callback, _mpr_connectclient, routprot/ConnectClient, rras.connectclient
ms.topic: callback
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
 - ConnectClient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PCONNECT_CLIENT callback function


## -description


The router manager calls the 
<b>ConnectClient</b> function when a client connects to an interface on which the routing protocol is running.

The <a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">PCONNECT_CLIENT</a> type defines a pointer to this callback function. <i>ConnectClient</i> is a placeholder for the application-defined function name.


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




<a href="https://msdn.microsoft.com/45859605-2981-4236-9546-9b88e07673fe">DisconnectClient</a>
 

 

