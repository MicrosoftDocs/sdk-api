---
UID: NS:raseapif._PPP_EAP_PACKET
title: PPP_EAP_PACKET (raseapif.h)
description: The PPP_EAP_PACKET structure specifies information about a packet being processed by the authentication protocol.
helpviewer_keywords: ["*PPPP_EAP_PACKET","EAPCODE_Failure","EAPCODE_Request","EAPCODE_Response","EAPCODE_Success","PPPP_EAP_PACKET","PPPP_EAP_PACKET structure pointer [EAP]","PPP_EAP_PACKET","PPP_EAP_PACKET structure [EAP]","_eap_ppp_eap_packet","eap.ppp_eap_packet","raseapif/PPPP_EAP_PACKET","raseapif/PPP_EAP_PACKET"]
old-location: eap\ppp_eap_packet.htm
tech.root: EAP
ms.assetid: a1ca16d1-bf91-4986-a4f8-6e6ad382730f
ms.date: 12/05/2018
ms.keywords: '*PPPP_EAP_PACKET, EAPCODE_Failure, EAPCODE_Request, EAPCODE_Response, EAPCODE_Success, PPPP_EAP_PACKET, PPPP_EAP_PACKET structure pointer [EAP], PPP_EAP_PACKET, PPP_EAP_PACKET structure [EAP], _eap_ppp_eap_packet, eap.ppp_eap_packet, raseapif/PPPP_EAP_PACKET, raseapif/PPP_EAP_PACKET'
req.header: raseapif.h
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
req.typenames: PPP_EAP_PACKET, *PPPP_EAP_PACKET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PPP_EAP_PACKET
 - raseapif/_PPP_EAP_PACKET
 - PPPP_EAP_PACKET
 - raseapif/PPPP_EAP_PACKET
 - PPP_EAP_PACKET
 - raseapif/PPP_EAP_PACKET
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Raseapif.h
api_name:
 - PPP_EAP_PACKET
---

# PPP_EAP_PACKET structure


## -description

The 
<b>PPP_EAP_PACKET</b> structure specifies information about a packet being processed by the authentication protocol.

## -struct-fields

### -field Code

Specifies the type of packet that is sent or received by the authentication protocol. This parameter is one of the four following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EAPCODE_Request"></a><a id="eapcode_request"></a><a id="EAPCODE_REQUEST"></a><dl>
<dt><b>EAPCODE_Request</b></dt>
</dl>
</td>
<td width="60%">
The packet is a request.

</td>
</tr>
<tr>
<td width="40%"><a id="EAPCODE_Response"></a><a id="eapcode_response"></a><a id="EAPCODE_RESPONSE"></a><dl>
<dt><b>EAPCODE_Response</b></dt>
</dl>
</td>
<td width="60%">
The packet is a response.

</td>
</tr>
<tr>
<td width="40%"><a id="EAPCODE_Success"></a><a id="eapcode_success"></a><a id="EAPCODE_SUCCESS"></a><dl>
<dt><b>EAPCODE_Success</b></dt>
</dl>
</td>
<td width="60%">
The packet indicates success.

</td>
</tr>
<tr>
<td width="40%"><a id="EAPCODE_Failure"></a><a id="eapcode_failure"></a><a id="EAPCODE_FAILURE"></a><dl>
<dt><b>EAPCODE_Failure</b></dt>
</dl>
</td>
<td width="60%">
The packet indicates failure.

</td>
</tr>
</table>

### -field Id

Specifies the identifier of the packet. The authentication protocol is responsible for maintaining packet counts for sessions, as that packet count pertains to EAP activity.

### -field Length

Specifies the length of the packet.

### -field Data

Specifies the data transmitted by this packet. If the packet is a request or a response packet, the first byte of this member signifies its type. For more information about packet types and requirements for type reservation, refer to 
<a href="https://www.ietf.org/rfc/rfc2284.txt">RFC 2284</a>.

## -see-also

[EAP Structures](/windows/win32/eap/eap-structures)



[Extensible Authentication Protocol Reference](/windows/win32/eap/extensible-authentication-protocol-reference)



<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_info">PPP_EAP_INFO</a>



<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_input">PPP_EAP_INPUT</a>



<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_output">PPP_EAP_OUTPUT</a>



<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapgetinfo">RasEapGetInfo</a>



<a href="/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)">RasEapMakeMessage</a>