---
UID: NS:mstcpip._INET_PORT_RANGE
title: INET_PORT_RANGE (mstcpip.h)
description: Provides input data used by the SIO_ACQUIRE_PORT_RESERVATION IOCTL to acquire a runtime reservation for a block of TCP or UDP ports.
helpviewer_keywords: ["*PINET_PORT_RANGE","*PINET_PORT_RESERVATION","INET_PORT_RANGE","INET_PORT_RANGE structure [Winsock]","INET_PORT_RESERVATION","PINET_PORT_RANGE","PINET_PORT_RANGE structure pointer [Winsock]","mstcpip/INET_PORT_RANGE","mstcpip/PINET_PORT_RANGE","winsock.inet_port_range"]
old-location: winsock\inet_port_range.htm
tech.root: WinSock
ms.assetid: FE6946CF-61B6-422C-B9B8-5045EFAB705F
ms.date: 12/05/2018
ms.keywords: '*PINET_PORT_RANGE, *PINET_PORT_RESERVATION, INET_PORT_RANGE, INET_PORT_RANGE structure [Winsock], INET_PORT_RESERVATION, PINET_PORT_RANGE, PINET_PORT_RANGE structure pointer [Winsock], mstcpip/INET_PORT_RANGE, mstcpip/PINET_PORT_RANGE, winsock.inet_port_range'
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
req.typenames: INET_PORT_RANGE, *PINET_PORT_RANGE, INET_PORT_RESERVATION, *PINET_PORT_RESERVATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INET_PORT_RANGE
 - mstcpip/_INET_PORT_RANGE
 - PINET_PORT_RANGE
 - mstcpip/PINET_PORT_RANGE
 - INET_PORT_RANGE
 - mstcpip/INET_PORT_RANGE
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
 - INET_PORT_RANGE
---

# INET_PORT_RANGE structure


## -description

The <b>INET_PORT_RANGE</b> structure provides input data used by the <a href="/windows/win32/winsock/sio-acquire-port-reservation">SIO_ACQUIRE_PORT_RESERVATION</a> IOCTL to acquire a runtime reservation for a block of TCP or UDP ports.

## -struct-fields

### -field StartPort

The starting TCP or UDP port number. If this parameter is set to zero, the system will choose a starting TCP or UDP port number.

### -field NumberOfPorts

The number of TCP or UDP port numbers to reserve.

## -remarks

The  <b>INET_PORT_RANGE</b> structure is supported on Windows Vista and later.

The 
<b>INET_PORT_RANGE</b> structure is the datatype passed in the input buffer to the <a href="/windows/win32/winsock/sio-acquire-port-reservation">SIO_ACQUIRE_PORT_RESERVATION</a> IOCTL. This IOCTL is used to acquire a runtime reservation for a block of TCP or UDP ports.  

The 
<b>INET_PORT_RANGE</b> structure is typedefed to the <b>INET_PORT_RESERVATION</b> structure.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation">CreatePersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation">CreatePersistentUdpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation">DeletePersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation">DeletePersistentUdpPortReservation</a>



<a href="/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance">INET_PORT_RESERVATION_INSTANCE</a>



<a href="/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token">INET_PORT_RESERVATION_TOKEN</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation">LookupPersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation">LookupPersistentUdpPortReservation</a>



<a href="/windows/win32/winsock/sio-acquire-port-reservation">SIO_ACQUIRE_PORT_RESERVATION</a>



<a href="/windows/win32/winsock/sio-associate-port-reservation">SIO_ASSOCIATE_PORT_RESERVATION</a>



<a href="/windows/win32/winsock/sio-release-port-reservation">SIO_RELEASE_PORT_RESERVATION</a>