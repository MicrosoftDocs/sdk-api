---
UID: NS:ws2atm.sockaddr_atm
title: sockaddr_atm (ws2atm.h)
description: The Windows Sockets sockaddr_atm structure stores socket address information for ATM sockets.
helpviewer_keywords: ["*LPSOCKADDR_ATM","*PSOCKADDR_ATM","LPSOCKADDR_ATM","LPSOCKADDR_ATM structure pointer [Winsock]","PSOCKADDR_ATM","PSOCKADDR_ATM structure pointer [Winsock]","SOCKADDR_ATM","SOCKADDR_ATM structure [Winsock]","_win32_sockaddr_atm_2","sockaddr_atm","sockaddr_atm structure [Winsock]","winsock.sockaddr_atm_2","ws2atm/LPSOCKADDR_ATM","ws2atm/PSOCKADDR_ATM","ws2atm/SOCKADDR_ATM","ws2atm/sockaddr_atm"]
old-location: winsock\sockaddr_atm_2.htm
tech.root: WinSock
ms.assetid: 6cbeb19f-0aa8-48a1-a46a-691edc542d5a
ms.date: 12/05/2018
ms.keywords: '*LPSOCKADDR_ATM, *PSOCKADDR_ATM, LPSOCKADDR_ATM, LPSOCKADDR_ATM structure pointer [Winsock], PSOCKADDR_ATM, PSOCKADDR_ATM structure pointer [Winsock], SOCKADDR_ATM, SOCKADDR_ATM structure [Winsock], _win32_sockaddr_atm_2, sockaddr_atm, sockaddr_atm structure [Winsock], winsock.sockaddr_atm_2, ws2atm/LPSOCKADDR_ATM, ws2atm/PSOCKADDR_ATM, ws2atm/SOCKADDR_ATM, ws2atm/sockaddr_atm'
req.header: ws2atm.h
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
req.typenames: sockaddr_atm, SOCKADDR_ATM, *PSOCKADDR_ATM, *LPSOCKADDR_ATM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - sockaddr_atm
 - ws2atm/sockaddr_atm
 - PSOCKADDR_ATM
 - ws2atm/PSOCKADDR_ATM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2atm.h
api_name:
 - sockaddr_atm
---

# sockaddr_atm structure


## -description

The Windows Sockets 
<b>sockaddr_atm</b> structure stores socket address information for ATM sockets.

## -struct-fields

### -field satm_family

Identifies the address family, which is AF_ATM in this case.

### -field satm_number

Identifies the ATM address that could be either in E.164 or NSAP-style ATM End Systems Address format.  This field will be mapped to the called party number information element (IE) if it is specified in 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> and 
<a href="/previous-versions/windows/hardware/network/ff566268(v=vs.85)">WSPBind</a> for a listening socket, or in 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>, 
<a href="/previous-versions/windows/hardware/network/ff566275(v=vs.85)">WSPConnect</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsajoinleaf">WSAJoinLeaf</a>, or
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpwspjoinleaf">WSPJoinLeaf</a> for a connecting socket. It will be mapped to the Calling Party Number IE if specified in 
<b>bind</b> and 
<b>WSPBind</b> for a connecting socket.

### -field satm_blli

Identifies the fields in the B-LLI information element that are used along with <b>satm_bhli</b> to identify an application. See 
<a href="/windows/desktop/api/ws2atm/ns-ws2atm-atm_blli">ATM_BLLI</a> for more details. Note that the B-LLI layer two information is treated as not present if its <b>Layer2Protocol</b> field contains SAP_FIELD_ABSENT, or as a wildcard if it contains SAP_FIELD_ANY. Similarly, the B-LLI layer three information is treated as not present if its <b>Layer3Protocol</b> field contains SAP_FIELD_ABSENT, or as a wildcard if it contains SAP_FIELD_ANY.

### -field satm_bhli

Identifies the fields in the B-HLI information element that are used along with <b>satm_blli</b> to identify an application. See 
<a href="/windows/desktop/api/ws2atm/ns-ws2atm-atm_bhli">ATM_BHLI</a> for information about the 
<b>ATM_BHLI</b> structure. 





<div class="alert"><b>Note</b>  <b>satm_bhli</b> is treated as not present if its <b>HighLayerInfoType</b> field contains SAP_FIELD_ABSENT, or as a wildcard if it contains SAP_FIELD_ANY.</div>
<div> </div>

## -remarks

For listening sockets, the <b>sockaddr_atm</b> structure is used in 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>/<a href="/previous-versions/windows/hardware/network/ff566268(v=vs.85)">WSPBind</a> to register a Service Access Point (SAP) to receive incoming connection requests destined to this SAP. SAP registration is used to match against the SAP specified in an incoming connection request  to determine which listening socket is to receive this request. In the current  specification, overlapping registration is not allowed. Overlapping registration is defined as having more than one registered SAP to potentially match the SAP specified in any incoming connection request. 
<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">Listen</a> and 
<a href="/previous-versions/windows/hardware/network/ff566297(v=vs.85)">WSPListen</a> will return the error code WSAEADDRINUSE if the SAP associated with the listening socket overlaps with any currently registered SAPs in the system.

The fields in a SAP to be registered must contain either a valid value, or one of two special manifest constants: SAP_FIELD_ABSENT or SAP_FIELD_ANY.

SAP_FIELD_ABSENT simply means that this field is not presented as part of a SAP. SAP_FIELD_ANY means using wildcards.

Note that the requirement of nonoverlapping registration does not preclude using wildcards. For example, it is possible to have two registered SAPs that both contain SAP_FIELD_ANY in some fields and different values in other fields.

<div class="alert"><b>Note</b>  The called party ATM number is mandatory, thus the <b>satm_number</b> field cannot contain SAP_FIELD_ABSENT.</div>
<div> </div>
For connecting sockets, the <b>sockaddr_atm</b> structure is used to specify the destination SAP in 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>/<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>/<a href="/previous-versions/windows/hardware/network/ff566275(v=vs.85)">WSPConnect</a> for point-to-point connections, and 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsajoinleaf">WSAJoinLeaf</a>/<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpwspjoinleaf">WSPJoinLeaf</a> for point-to-multipoint connections. The fields in the destination SAP of a connecting socket must contain either a valid value or SAP_FIELD_ABSENT, that is, SAP_FIELD_ANY is not allowed.

Furthermore, SAP_FIELD_ABSENT is not allowed for the <b>satm_number</b> field. The destination SAP is used to match against all the registered SAPs in the destination computer to determine the forwarding destination for this connection request. If each and every field of the destination SAP of an incoming request either equals the corresponding field of a registered SAP, or the corresponding field contains the SAP_FIELD_ANY, the listening socket associated with this registered SAP will receive the incoming connection request.

If 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> and/or 
<a href="/previous-versions/windows/hardware/network/ff566268(v=vs.85)">WSPBind</a> are used on a connecting socket to specify the calling party ATM address, the <b>satm_blli</b> and <b>satm_bhli</b> fields should be ignored and the ones specified in 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>, or 
<a href="/previous-versions/windows/hardware/network/ff566275(v=vs.85)">WSPConnect</a> will be used.

## -see-also

<a href="/windows/desktop/api/ws2atm/ns-ws2atm-atm_address">ATM_ADDRESS</a>



<a href="/windows/desktop/api/ws2atm/ns-ws2atm-atm_bhli">ATM_BHLI</a>



<a href="/windows/desktop/api/ws2atm/ns-ws2atm-atm_blli">ATM_BLLI</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsajoinleaf">WSAJoinLeaf</a>



<a href="/previous-versions/windows/hardware/network/ff566268(v=vs.85)">WSPBind</a>



<a href="/previous-versions/windows/hardware/network/ff566275(v=vs.85)">WSPConnect</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpwspjoinleaf">WSPJoinLeaf</a>



<a href="/previous-versions/windows/hardware/network/ff566297(v=vs.85)">WSPListen</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a>