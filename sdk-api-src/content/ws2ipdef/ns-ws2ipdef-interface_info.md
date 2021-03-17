---
UID: NS:ws2ipdef._INTERFACE_INFO
title: INTERFACE_INFO (ws2ipdef.h)
description: The INTERFACE_INFO structure is used in conjunction with the SIO_GET_INTERFACE_LIST ioctl command to obtain information about an interface IP address.
helpviewer_keywords: ["*LPINTERFACE_INFO","IFF_BROADCAST","IFF_LOOPBACK","IFF_MULTICAST","IFF_POINTTOPOINT","IFF_UP","INTERFACE_INFO","INTERFACE_INFO structure [Winsock]","INTERFACE_INFO","FAR * LPINTERFACE_INFO","INTERFACE_INFO","FAR * LPINTERFACE_INFO structure [Winsock]","_win32_interface_info_2","winsock.interface_info_2","ws2ipdef/INTERFACE_INFO","ws2tcpip/INTERFACE_INFO"]
old-location: winsock\interface_info_2.htm
tech.root: WinSock
ms.assetid: fe1bf38d-70a7-4f0a-b76a-c0c9443d1782
ms.date: 12/05/2018
ms.keywords: '*LPINTERFACE_INFO, IFF_BROADCAST, IFF_LOOPBACK, IFF_MULTICAST, IFF_POINTTOPOINT, IFF_UP, INTERFACE_INFO, INTERFACE_INFO structure [Winsock], INTERFACE_INFO,FAR * LPINTERFACE_INFO, INTERFACE_INFO,FAR * LPINTERFACE_INFO structure [Winsock], _win32_interface_info_2, winsock.interface_info_2, ws2ipdef/INTERFACE_INFO, ws2tcpip/INTERFACE_INFO'
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
req.typenames: INTERFACE_INFO, *LPINTERFACE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INTERFACE_INFO
 - ws2ipdef/_INTERFACE_INFO
 - LPINTERFACE_INFO
 - ws2ipdef/LPINTERFACE_INFO
 - INTERFACE_INFO
 - ws2ipdef/INTERFACE_INFO
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
 - INTERFACE_INFO, FAR * LPINTERFACE_INFO
---

# INTERFACE_INFO structure


## -description

The 
<b>INTERFACE_INFO</b> structure is used in conjunction with the <b>SIO_GET_INTERFACE_LIST</b> ioctl command to obtain information about an interface IP address.

## -struct-fields

### -field iiFlags

A bitmask describing the status of the interface. The following flags are possible.

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

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>INTERFACE_INFO</b> structure is defined in the <i>Ws2ipdef.h</i> header file which is automatically included in the <i>Ws2tcpip.h</i> header file. The <i>Ws2ipdef.h</i>  header files should never be used directly.

## -see-also

<a href="/windows/desktop/WinSock/winsock-ioctls">Winsock IOCTLs</a>