---
UID: NS:mstcpip.INET_PORT_RESERVATION_TOKEN
title: INET_PORT_RESERVATION_TOKEN (mstcpip.h)
description: Contains a port reservation token for a block of TCP or UDP ports.
helpviewer_keywords: ["*PINET_PORT_RESERVATION_TOKEN","INET_PORT_RESERVATION_TOKEN","INET_PORT_RESERVATION_TOKEN structure [Winsock]","PINET_PORT_RESERVATION_TOKEN","PINET_PORT_RESERVATION_TOKEN structure pointer [Winsock]","mstcpip/INET_PORT_RESERVATION_TOKEN","mstcpip/PINET_PORT_RESERVATION_TOKEN","winsock.inet_port_reservation_token"]
old-location: winsock\inet_port_reservation_token.htm
tech.root: WinSock
ms.assetid: 1AA2FF8C-BEAB-4D38-B53A-68E0628748FF
ms.date: 12/05/2018
ms.keywords: '*PINET_PORT_RESERVATION_TOKEN, INET_PORT_RESERVATION_TOKEN, INET_PORT_RESERVATION_TOKEN structure [Winsock], PINET_PORT_RESERVATION_TOKEN, PINET_PORT_RESERVATION_TOKEN structure pointer [Winsock], mstcpip/INET_PORT_RESERVATION_TOKEN, mstcpip/PINET_PORT_RESERVATION_TOKEN, winsock.inet_port_reservation_token'
req.header: mstcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: INET_PORT_RESERVATION_TOKEN, *PINET_PORT_RESERVATION_TOKEN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PINET_PORT_RESERVATION_TOKEN
 - mstcpip/PINET_PORT_RESERVATION_TOKEN
 - INET_PORT_RESERVATION_TOKEN
 - mstcpip/INET_PORT_RESERVATION_TOKEN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstcpip.h
api_name:
 - INET_PORT_RESERVATION_TOKEN
---

# INET_PORT_RESERVATION_TOKEN structure


## -description

The <b>INET_PORT_RESERVATION_TOKEN</b> structure contains a port reservation token for a block of TCP or UDP ports.

## -struct-fields

### -field Token

A port reservation token for a block of TCP or UDP ports.

## -remarks

The  <b>INET_PORT_RESERVATION_TOKEN</b> structure is supported on Windows Vista and later.

The  <b>INET_PORT_RESERVATION_TOKEN</b> structure is used by the <a href="/windows/win32/winsock/sio-acquire-port-reservation">SIO_ACQUIRE_PORT_RESERVATION</a> , <a href="/windows/win32/winsock/sio-associate-port-reservation">SIO_ASSOCIATE_PORT_RESERVATION</a>, and <a href="/windows/win32/winsock/sio-release-port-reservation">SIO_RELEASE_PORT_RESERVATION</a> Ioctl for TCP or UDP port reservations.  The <b>INET_PORT_RESERVATION_TOKEN</b> structure is also equivalent to the ULONG64 Token parameter used by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation">CreatePersistentTcpPortReservation</a>, <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation">CreatePersistentUdpPortReservation</a>, <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation">DeletePersistentTcpPortReservation</a>, <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation">DeletePersistentUdpPortReservation</a>, <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation">LookupPersistentTcpPortReservation</a>, and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation">LookupPersistentUdpPortReservation</a> functions in IP Helper.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation">CreatePersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation">CreatePersistentUdpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation">DeletePersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation">DeletePersistentUdpPortReservation</a>



<a href="/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range">INET_PORT_RANGE</a>



<a href="/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance">INET_PORT_RESERVATION_INSTANCE</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation">LookupPersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation">LookupPersistentUdpPortReservation</a>



<a href="/windows/win32/winsock/sio-acquire-port-reservation">SIO_ACQUIRE_PORT_RESERVATION</a>



<a href="/windows/win32/winsock/sio-associate-port-reservation">SIO_ASSOCIATE_PORT_RESERVATION</a>



<a href="/windows/win32/winsock/sio-release-port-reservation">SIO_RELEASE_PORT_RESERVATION</a>

