---
UID: NS:nspapi._SERVICE_ADDRESS
title: SERVICE_ADDRESS (nspapi.h)
description: Contains address information for a service. The structure can accommodate many types of interprocess communications (IPC) mechanisms and their address forms, including remote procedure calls (RPC), named pipes, and sockets.
helpviewer_keywords: ["*LPSERVICE_ADDRESS","*PSERVICE_ADDRESS","SERVICE_ADDRESS","SERVICE_ADDRESS structure [Winsock]","SERVICE_ADDRESS_FLAG_RPC_CN","SERVICE_ADDRESS_FLAG_RPC_DG","SERVICE_ADDRESS_FLAG_RPC_NB","_win32_service_address_2","nspapi/SERVICE_ADDRESS","winsock.service_address_2"]
old-location: winsock\service_address_2.htm
tech.root: WinSock
ms.assetid: 5fc99e3a-7316-4950-9249-968bbc4168c2
ms.date: 12/05/2018
ms.keywords: '*LPSERVICE_ADDRESS, *PSERVICE_ADDRESS, SERVICE_ADDRESS, SERVICE_ADDRESS structure [Winsock], SERVICE_ADDRESS_FLAG_RPC_CN, SERVICE_ADDRESS_FLAG_RPC_DG, SERVICE_ADDRESS_FLAG_RPC_NB, _win32_service_address_2, nspapi/SERVICE_ADDRESS, winsock.service_address_2'
req.header: nspapi.h
req.include-header: 
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
targetos: Windows
req.typenames: SERVICE_ADDRESS, *PSERVICE_ADDRESS, *LPSERVICE_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_ADDRESS
 - nspapi/_SERVICE_ADDRESS
 - PSERVICE_ADDRESS
 - nspapi/PSERVICE_ADDRESS
 - SERVICE_ADDRESS
 - nspapi/SERVICE_ADDRESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nspapi.h
api_name:
 - SERVICE_ADDRESS
---

# SERVICE_ADDRESS structure


## -description

The 
<b>SERVICE_ADDRESS</b> structure contains address information for a service. The structure can accommodate many types of interprocess communications (IPC) mechanisms and their address forms, including remote procedure calls (RPC), named pipes, and sockets.

## -struct-fields

### -field dwAddressType

Type: <b>DWORD</b>

The address family to which the socket address pointed to by <b>lpAddress</b> member belongs.

### -field dwAddressFlags

Type: <b>DWORD</b>

A set of bit flags that specify properties of the address. The following bit flags are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ADDRESS_FLAG_RPC_CN"></a><a id="service_address_flag_rpc_cn"></a><dl>
<dt><b>SERVICE_ADDRESS_FLAG_RPC_CN</b></dt>
</dl>
</td>
<td width="60%">
If this bit flag is set, the service supports connection-oriented RPC over this transport protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ADDRESS_FLAG_RPC_DG"></a><a id="service_address_flag_rpc_dg"></a><dl>
<dt><b>SERVICE_ADDRESS_FLAG_RPC_DG</b></dt>
</dl>
</td>
<td width="60%">
If this bit flag is set, the service supports datagram-oriented RPC over this transport protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ADDRESS_FLAG_RPC_NB"></a><a id="service_address_flag_rpc_nb"></a><dl>
<dt><b>SERVICE_ADDRESS_FLAG_RPC_NB</b></dt>
</dl>
</td>
<td width="60%">
If this bit flag is set, the service supports NetBIOS RPC over this transport protocol.

</td>
</tr>
</table>

### -field dwAddressLength

Type: <b>DWORD</b>

The size, in bytes, of the address.

### -field dwPrincipalLength

Type: <b>DWORD</b>

Reserved for future use. Must be zero.

### -field lpAddress.size_is

### -field lpAddress.size_is.dwAddressLength

### -field lpAddress

Type: <b>BYTE*</b>

A pointer to a socket address of the appropriate type.

### -field lpPrincipal.size_is

### -field lpPrincipal.size_is.dwPrincipalLength

### -field lpPrincipal

Type: <b>BYTE*</b>

Reserved for future use. Must be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/nspapi/ns-nspapi-service_addresses">SERVICE_ADDRESSES</a>



<a href="/windows/desktop/api/nspapi/ns-nspapi-service_infoa">SERVICE_INFO</a>