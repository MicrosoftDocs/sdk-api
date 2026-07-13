---
UID: NS:wtsapi32._WTS_CLIENT_ADDRESS
title: WTS_CLIENT_ADDRESS (wtsapi32.h)
description: Contains the client network address of a Remote Desktop Services session.
helpviewer_keywords: ["*PWTS_CLIENT_ADDRESS","PWTS_CLIENT_ADDRESS","PWTS_CLIENT_ADDRESS structure pointer [Remote Desktop Services]","WTS_CLIENT_ADDRESS","WTS_CLIENT_ADDRESS structure [Remote Desktop Services]","_win32_wts_client_address_str","termserv.wts_client_address_str","wtsapi32/PWTS_CLIENT_ADDRESS","wtsapi32/WTS_CLIENT_ADDRESS"]
old-location: termserv\wts_client_address_str.htm
tech.root: TermServ
ms.assetid: 29034986-f8d1-4cf0-9f53-e4b195d450a6
ms.date: 12/05/2018
ms.keywords: '*PWTS_CLIENT_ADDRESS, PWTS_CLIENT_ADDRESS, PWTS_CLIENT_ADDRESS structure pointer [Remote Desktop Services], WTS_CLIENT_ADDRESS, WTS_CLIENT_ADDRESS structure [Remote Desktop Services], _win32_wts_client_address_str, termserv.wts_client_address_str, wtsapi32/PWTS_CLIENT_ADDRESS, wtsapi32/WTS_CLIENT_ADDRESS'
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WTS_CLIENT_ADDRESS, *PWTS_CLIENT_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_CLIENT_ADDRESS
 - wtsapi32/_WTS_CLIENT_ADDRESS
 - PWTS_CLIENT_ADDRESS
 - wtsapi32/PWTS_CLIENT_ADDRESS
 - WTS_CLIENT_ADDRESS
 - wtsapi32/WTS_CLIENT_ADDRESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTS_CLIENT_ADDRESS
---

# WTS_CLIENT_ADDRESS structure


## -description

Contains 
    the client network address of a Remote Desktop Services session.

## -struct-fields

### -field AddressFamily

Address family. This member can be <b>AF_INET</b>, <b>AF_INET6</b>, <b>AF_IPX</b>, <b>AF_NETBIOS</b>, or <b>AF_UNSPEC</b>.

### -field Address

Client network address. The format of the field of <b>Address</b> depends on the address type as specified by the <b>AddressFamily</b> member.

For an address family **AF_INET**: **Address** contains the IPV4 address of the client as raw byte values. The IP address is offset by two bytes from the start of the Address member. For example, the address 192.168.0.1 would be represented as the following series of byte values: "0x00 0x00 0xC0 0xA8 0x00 0x01".


For a family <b>AF_INET6</b>: <b>Address </b> contains the IPV6 address of the client as raw byte values. (For example, the address "FFFF::1" would be represented as the following series of byte values: "0xFF 0xFF 0x00 0x00  0x00 0x00  0x00 0x00  0x00 0x00  0x00 0x00  0x00 0x00  0x00 0x01")

## -remarks

The client network address is reported by the RDP client itself when it connects to the server. This could be different than the address that actually connected to the server. For example, suppose there is a NAT between the client and the server. The client can report its own IP address, but the IP address that actually connects to the server is the NAT address. For VPN connections, the IP address might not be discoverable by the client. If it cannot be discovered, the client can report the only IP address it has, which may be the ISP assigned address. Because the address may not be the actual network address, it should not be used as a form of client authentication.
    
The client network address is also not available in the following cases:
- The connection is established through a Remote Desktop Gateway.
- The connection is originated by the **Microsoft Remote Desktop** app that is available in the Store.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a>
