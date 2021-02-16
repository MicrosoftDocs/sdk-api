---
UID: NS:ws2bth._SOCKADDR_BTH
title: SOCKADDR_BTH (ws2bth.h)
description: The SOCKADDR_BTH structure is used in conjunction with Bluetooth socket operations, defined by address family AF_BTH.
helpviewer_keywords: ["*PSOCKADDR_BTH","PSOCKADDR_BTH","PSOCKADDR_BTH structure pointer [Bluetooth]","SOCKADDR_BTH","SOCKADDR_BTH structure [Bluetooth]","_bth_sockaddr_bth","bluetooth.sockaddr_bth","ws2bth/PSOCKADDR_BTH","ws2bth/SOCKADDR_BTH"]
old-location: bluetooth\sockaddr_bth.htm
tech.root: bluetooth
ms.assetid: e8eefa1d-94fa-45f3-a7c2-ea12a372a43b
ms.date: 12/05/2018
ms.keywords: '*PSOCKADDR_BTH, PSOCKADDR_BTH, PSOCKADDR_BTH structure pointer [Bluetooth], SOCKADDR_BTH, SOCKADDR_BTH structure [Bluetooth], _bth_sockaddr_bth, bluetooth.sockaddr_bth, ws2bth/PSOCKADDR_BTH, ws2bth/SOCKADDR_BTH'
req.header: ws2bth.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: SOCKADDR_BTH, *PSOCKADDR_BTH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SOCKADDR_BTH
 - ws2bth/_SOCKADDR_BTH
 - PSOCKADDR_BTH
 - ws2bth/PSOCKADDR_BTH
 - SOCKADDR_BTH
 - ws2bth/SOCKADDR_BTH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2bth.h
api_name:
 - SOCKADDR_BTH
---

# SOCKADDR_BTH structure


## -description

The 
<b>SOCKADDR_BTH</b> structure is used in conjunction with Bluetooth socket operations, defined by address family AF_BTH.

## -struct-fields

### -field addressFamily

Address family of the socket. This member is always AF_BTH.

### -field btAddr

Address of the target Bluetooth device. When used with the 
<a href="/windows/desktop/Bluetooth/bluetooth-and-bind">bind</a> function, must be zero or a valid local radio address. If zero, a valid local Bluetooth device address is assigned when the 
<a href="/windows/desktop/Bluetooth/bluetooth-and-connect">connect</a> or 
<a href="/windows/desktop/Bluetooth/bluetooth-and-accept">accept</a> function is called. When used with the <b>connect</b> function, a valid remote radio address must be specified.

### -field serviceClassId

Service Class Identifier of the socket. When used with the <a href="/windows/desktop/Bluetooth/bluetooth-and-bind">bind</a> function, <i>serviceClassId</i> is ignored. Also ignored if the port is specified. For the <a href="/windows/desktop/Bluetooth/bluetooth-and-connect">connect</a> function, specifies the unique Bluetooth service class ID of the service to which it wants to connect. If the peer device has more than one port that corresponds to the service class identifier, the <b>connect</b> function attempts to connect to the first valid service; this mechanism can be used without prior SDP queries.

### -field port

RFCOMM channel associated with the socket. See Remarks.

## -remarks

When used with the <a href="/windows/desktop/Bluetooth/bluetooth-and-bind">bind</a> function on client applications, the <b>port</b> member must be zero to enable an appropriate local endpoint to be assigned. When used with <b>bind</b> on server applications, the <b>port</b> member must be a valid port number or BT_PORT_ANY; ports automatically assigned using BT_PORT_ANY may be queried subsequently with a call to the <a href="/windows/desktop/Bluetooth/bluetooth-and-getsockname">getsockname</a> function. The valid range for requesting a specific RFCOMM port is 1 through 30.

When using the <a href="/windows/desktop/Bluetooth/bluetooth-and-connect">connect</a> function when <b>serviceClassId</b> is not provided, the port should directly specify the remote port number to which a <b>connect</b> operation is requested. Using the <b>port</b> member instead of the <b>serviceClassId</b> member requires the application  to perform its own service (SDP) search before attempting the <b>connect</b> operation.

## -see-also

<a href="/windows/desktop/Bluetooth/bluetooth-and-bind">Bluetooth
		  and bind</a>



<a href="/windows/desktop/Bluetooth/bluetooth-and-getsockname">Bluetooth
		  and getsockname</a>



<a href="/windows/desktop/Bluetooth/bluetooth-and-accept">Bluetooth and
		  accept</a>



<a href="/windows/desktop/Bluetooth/bluetooth-and-connect">Bluetooth and
		  connect</a>