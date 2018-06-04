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

# _WTS_CLIENT_ADDRESS structure


## -description


Contains 
    the client network address of a Remote Desktop Services session.


## -struct-fields




### -field AddressFamily

Address family. This member can be <b>AF_INET</b>, <b>AF_INET6</b>, <b>AF_IPX</b>, <b>AF_NETBIOS</b>, or <b>AF_UNSPEC</b>.


### -field Address

Client network address. The format of the field of <b>Address</b> depends on the address type as specified by the <b>AddressFamily</b> member.

For an address family <b>AF_INET</b>: <b>Address </b> contains the IPV4 address of the client as a null-terminated string.


For an family <b>AF_INET6</b>: <b>Address </b> contains the IPV6 address of the client as raw byte values. (For example, the address "FFFF::1" would be represented as the following series of byte values: "0xFF 0xFF 0x00 0x00  0x00 0x00  0x00 0x00  0x00 0x00  0x00 0x00  0x00 0x00  0x00 0x01")


## -remarks



The client network address is reported by the RDP client itself when it connects to the server. This could be 
    different than the address that actually connected to the server. For example, suppose there is a NAT between the 
    client and the server. The client can report its own IP address, but the IP address that actually connects to the 
    server is the NAT address. For VPN connections, the IP address might not be discoverable by the client. If it 
    cannot be discovered, the client can report the only IP address it has, which may be the ISP assigned address. 
    Because the address may not be the actual network address, it should not be used as a form of client 
    authentication.




## -see-also




<a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a>
 

 

