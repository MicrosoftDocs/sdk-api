---
UID: NS:lmserver._SERVER_TRANSPORT_INFO_0
title: SERVER_TRANSPORT_INFO_0 (lmserver.h)
author: windows-sdk-content
description: The SERVER_TRANSPORT_INFO_0 structure contains information about the specified transport protocol, including name, address, and location on the network.
old-location: netmgmt\server_transport_info_0_str.htm
tech.root: NetMgmt
ms.assetid: 5b94cf7a-74d1-4ae8-87bd-22b2daf292cb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPSERVER_TRANSPORT_INFO_0, *PSERVER_TRANSPORT_INFO_0, LPSERVER_TRANSPORT_INFO_0, LPSERVER_TRANSPORT_INFO_0 structure pointer [Network Management], PSERVER_TRANSPORT_INFO_0, PSERVER_TRANSPORT_INFO_0 structure pointer [Network Management], SERVER_TRANSPORT_INFO_0, SERVER_TRANSPORT_INFO_0 structure [Network Management], _win32_server_transport_info_0_str, lmserver/LPSERVER_TRANSPORT_INFO_0, lmserver/PSERVER_TRANSPORT_INFO_0, lmserver/SERVER_TRANSPORT_INFO_0, netmgmt.server_transport_info_0_str"
ms.topic: struct
req.header: lmserver.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
 - HeaderDef
api_location:
 - Lmserver.h
api_name:
 - SERVER_TRANSPORT_INFO_0
product: Windows
targetos: Windows
req.typenames: SERVER_TRANSPORT_INFO_0, *PSERVER_TRANSPORT_INFO_0, *LPSERVER_TRANSPORT_INFO_0
req.redist: 
---

# SERVER_TRANSPORT_INFO_0 structure


## -description


The
				<b>SERVER_TRANSPORT_INFO_0</b> structure contains information about the specified transport protocol, including name, address, and location on the network.


## -struct-fields




### -field svti0_numberofvcs

Type: <b>DWORD</b>

The number of clients connected to the server that are using the transport protocol specified by the <b>svti0_transportname</b> member.


### -field svti0_transportname

Type: <b>LMSTR</b>

A pointer to a NULL-terminated character string that contains the name of a transport device; for example,

<pre class="syntax" xml:space="preserve"><code>\Device\NetBT_Tcpip_{2C9725F4-151A-11D3-AEEC-C3B211BD350B}
</code></pre>
This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


### -field svti0_transportaddress

Type: <b>LPBYTE</b>

A pointer to a variable that contains the address the server is using on the transport device specified by the <b>svti0_transportname</b> member.

This member is usually the NetBIOS name that the server is using. In these instances, the name must be 16 characters long, and the last character must be a blank character (0x20).


### -field svti0_transportaddress.size_is

 


### -field svti0_transportaddress.size_is.svti0_transportaddresslength

 


### -field svti0_transportaddresslength

Type: <b>DWORD</b>

The length, in bytes, of the <b>svti0_transportaddress</b> member. For NetBIOS names, the value of this member is 16 (decimal).


### -field svti0_networkaddress

Type: <b>LMSTR</b>

A pointer to a NULL-terminated character string that contains the address the network adapter is using. The string is transport-specific.

You can retrieve this value only with a call to the 
<a href="https://msdn.microsoft.com/db42ac44-d70d-4b89-882a-6ac83fd611fd">NetServerTransportEnum</a> function. You cannot set this value with a call to the 
<a href="https://msdn.microsoft.com/c8521aed-0762-4412-b117-c911fc77049b">NetServerTransportAdd</a> function or the 
<a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a> function.)

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


## -remarks



The 
				<b>SERVER_TRANSPORT_INFO_0</b> structure is used by the <a href="https://msdn.microsoft.com/c8521aed-0762-4412-b117-c911fc77049b">NetServerTransportAdd</a> or <a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a> function to bind the specified server to the transport protocol.




## -see-also




<a href="https://msdn.microsoft.com/c8521aed-0762-4412-b117-c911fc77049b">NetServerTransportAdd</a>



<a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a>



<a href="https://msdn.microsoft.com/69b22f30-62b1-4dcb-bbb0-aceae8d77f61">NetServerTransportDel</a>



<a href="https://msdn.microsoft.com/db42ac44-d70d-4b89-882a-6ac83fd611fd">NetServerTransportEnum</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/f21fed49-207a-4f64-becd-3d3c1e995eb0">SERVER_TRANSPORT_INFO_1</a>



<a href="https://msdn.microsoft.com/b422eb71-1f93-432d-8283-81432edfe568">SERVER_TRANSPORT_INFO_2</a>



<a href="https://msdn.microsoft.com/045d60d4-518f-4ce4-b611-e23d1588d5d3">SERVER_TRANSPORT_INFO_3</a>



<a href="https://msdn.microsoft.com/64342e21-98f1-42d3-b541-46b826391fad">Server and Workstation Transport Functions</a>
 

 

