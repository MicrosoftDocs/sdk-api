---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _SOCKADDR_BTH structure


## -description



			The 
<b>SOCKADDR_BTH</b> structure is used in conjunction with Bluetooth socket operations, defined by address family AF_BTH.


## -struct-fields




### -field addressFamily

Address family of the socket. This member is always AF_BTH.


### -field btAddr

Address of the target Bluetooth device. When used with the 
<a href="https://msdn.microsoft.com/308d2680-de51-49e6-a0da-7aba494d9572">bind</a> function, must be zero or a valid local radio address. If zero, a valid local Bluetooth device address is assigned when the 
<a href="https://msdn.microsoft.com/f9ab3934-7698-4f5e-8194-cca86685a4f8">connect</a> or 
<a href="https://msdn.microsoft.com/79708118-2f70-4759-b5d6-cf5cfc33c27e">accept</a> function is called. When used with the <b>connect</b> function, a valid remote radio address must be specified.


### -field serviceClassId

Service Class Identifier of the socket. When used with the <a href="https://msdn.microsoft.com/308d2680-de51-49e6-a0da-7aba494d9572">bind</a> function, <i>serviceClassId</i> is ignored. Also ignored if the port is specified. For the <a href="https://msdn.microsoft.com/f9ab3934-7698-4f5e-8194-cca86685a4f8">connect</a> function, specifies the unique Bluetooth service class ID of the service to which it wants to connect. If the peer device has more than one port that corresponds to the service class identifier, the <b>connect</b> function attempts to connect to the first valid service; this mechanism can be used without prior SDP queries.


### -field port

RFCOMM channel associated with the socket. See Remarks.


## -remarks



When used with the <a href="https://msdn.microsoft.com/308d2680-de51-49e6-a0da-7aba494d9572">bind</a> function on client applications, the <b>port</b> member must be zero to enable an appropriate local endpoint to be assigned. When used with <b>bind</b> on server applications, the <b>port</b> member must be a valid port number or BT_PORT_ANY; ports automatically assigned using BT_PORT_ANY may be queried subsequently with a call to the <a href="https://msdn.microsoft.com/3892bd59-97ac-4b76-bff9-7329f22a66cc">getsockname</a> function. The valid range for requesting a specific RFCOMM port is 1 through 30.

When using the <a href="https://msdn.microsoft.com/f9ab3934-7698-4f5e-8194-cca86685a4f8">connect</a> function when <b>serviceClassId</b> is not provided, the port should directly specify the remote port number to which a <b>connect</b> operation is requested. Using the <b>port</b> member instead of the <b>serviceClassId</b> member requires the application  to perform its own service (SDP) search before attempting the <b>connect</b> operation.




## -see-also




<a href="https://msdn.microsoft.com/308d2680-de51-49e6-a0da-7aba494d9572">Bluetooth
		  and bind</a>



<a href="https://msdn.microsoft.com/3892bd59-97ac-4b76-bff9-7329f22a66cc">Bluetooth
		  and getsockname</a>



<a href="https://msdn.microsoft.com/79708118-2f70-4759-b5d6-cf5cfc33c27e">Bluetooth and
		  accept</a>



<a href="https://msdn.microsoft.com/f9ab3934-7698-4f5e-8194-cca86685a4f8">Bluetooth and
		  connect</a>
 

 

