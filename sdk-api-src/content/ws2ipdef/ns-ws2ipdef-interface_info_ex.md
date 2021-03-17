---
UID: NS:ws2ipdef._INTERFACE_INFO_EX
title: INTERFACE_INFO_EX (ws2ipdef.h)
description: The INTERFACE_INFO_EX structure is used in conjunction with the SIO_GET_INTERFACE_LIST IOCTL command to obtain information about an interface IP address.
helpviewer_keywords: ["*LPINTERFACE_INFO_EX","IFF_BROADCAST","IFF_LOOPBACK","IFF_MULTICAST","IFF_POINTTOPOINT","IFF_UP","INTERFACE_INFO_EX","INTERFACE_INFO_EX structure [Winsock]","INTERFACE_INFO_EX","FAR * _LPINTERFACE_INFO_EX","INTERFACE_INFO_EX","FAR * _LPINTERFACE_INFO_EX structure [Winsock]","winsock.interface_info_ex","ws2ipdef/INTERFACE_INFO_EX","ws2tcpip/INTERFACE_INFO_EX"]
old-location: winsock\interface_info_ex.htm
tech.root: WinSock
ms.assetid: d13a4b5d-9f61-464f-be50-ceda596cbb65
ms.date: 12/05/2018
ms.keywords: '*LPINTERFACE_INFO_EX, IFF_BROADCAST, IFF_LOOPBACK, IFF_MULTICAST, IFF_POINTTOPOINT, IFF_UP, INTERFACE_INFO_EX, INTERFACE_INFO_EX structure [Winsock], INTERFACE_INFO_EX,FAR * _LPINTERFACE_INFO_EX, INTERFACE_INFO_EX,FAR * _LPINTERFACE_INFO_EX structure [Winsock], winsock.interface_info_ex, ws2ipdef/INTERFACE_INFO_EX, ws2tcpip/INTERFACE_INFO_EX'
req.header: ws2ipdef.h
req.include-header: Ws2tcpip.h
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
req.typenames: INTERFACE_INFO_EX, *LPINTERFACE_INFO_EX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INTERFACE_INFO_EX
 - ws2ipdef/_INTERFACE_INFO_EX
 - LPINTERFACE_INFO_EX
 - ws2ipdef/LPINTERFACE_INFO_EX
 - INTERFACE_INFO_EX
 - ws2ipdef/INTERFACE_INFO_EX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2ipdef.h
 - Ws2tcpip.h
api_name:
 - INTERFACE_INFO_EX, FAR * _LPINTERFACE_INFO_EX
---

# INTERFACE_INFO_EX structure


## -description

The 
<b>INTERFACE_INFO_EX</b> structure is used in conjunction with the <b>SIO_GET_INTERFACE_LIST IOCTL</b> command to obtain information about an interface IP address. Unlike the <a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-interface_info">INTERFACE_INFO</a> structure, <b>INTERFACE_INFO_EX</b> is address-size independent, enabling it to work with IPv6.

## -struct-fields

### -field iiFlags

Bitmask describing the status of the interface. The following flags are possible.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IFF_UP"></a><a id="iff_up"></a><dl>
<dt><b>IFF_UP</b></dt>
</dl>
</td>
<td width="60%">
The interface is running.

</td>
</tr>
<tr>
<td width="40%"><a id="IFF_BROADCAST"></a><a id="iff_broadcast"></a><dl>
<dt><b>IFF_BROADCAST</b></dt>
</dl>
</td>
<td width="60%">
The broadcast feature is supported.

</td>
</tr>
<tr>
<td width="40%"><a id="IFF_LOOPBACK"></a><a id="iff_loopback"></a><dl>
<dt><b>IFF_LOOPBACK</b></dt>
</dl>
</td>
<td width="60%">
The loopback interface is running.

</td>
</tr>
<tr>
<td width="40%"><a id="IFF_POINTTOPOINT"></a><a id="iff_pointtopoint"></a><dl>
<dt><b>IFF_POINTTOPOINT</b></dt>
</dl>
</td>
<td width="60%">
The interface is using point-to-point link.

</td>
</tr>
<tr>
<td width="40%"><a id="IFF_MULTICAST"></a><a id="iff_multicast"></a><dl>
<dt><b>IFF_MULTICAST</b></dt>
</dl>
</td>
<td width="60%">
The multicast feature is supported.

</td>
</tr>
</table>

### -field iiAddress

Address of an interface.

### -field iiBroadcastAddress

Broadcast address of the interface or the address of the other side for point-to-point links.

### -field iiNetmask

Netmask used by the interface.

## -remarks

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>INTERFACE_INFO_EX</b> structure is defined in the <i>Ws2ipdef.h</i> header file which is automatically included in the <i>Ws2tcpip.h</i> header file. The <i>Ws2ipdef.h</i>  header files should never be used directly.

## -see-also

<a href="/windows/desktop/WinSock/winsock-ioctls">Winsock IOCTLs</a>